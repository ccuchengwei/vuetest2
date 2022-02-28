<template>
  <div>
    <div row>
    <h5  v-bind:class="[textClass]">{{title}}</h5>
    <b-table
      :striped="striped"
      :bordered="bordered"
      :borderless="borderless"
      :outlined="outlined"
      :small="small"
      :hover="hover"
      :dark="dark"
      :fixed="fixed"
      :foot-clone="footClone"
      :no-border-collapse="noCollapse"
      :items="parentItems"
      
      :head-variant="headVariant"
      :table-variant="tableVariant"
    ></b-table>
    </div>
  </div>
</template>

<script>
  export default {
    name: 'AmoebaTable',
    props: {
        parentItems : String,
        title : String,
        textClass : {
            type: String,
            default: 'text-primary'
        }
    },
    data() {
     return {
        
        striped: false,
        bordered: false,
        borderless: false,
        outlined: false,
        small: false,
        hover: false,
        dark: false,
        fixed: false,
        footClone: false,
        headVariant: 'dark',
        tableVariant: '',
        noCollapse: false,
        // textClass : 'text-primary'
      }
    }
    
  }
</script>