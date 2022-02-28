<template>
    <div>
        <header-nav></header-nav>
        <amoeba-table title='Runnning Job'  textClass='text-success' :parentItems="runningJob"></amoeba-table>
        <amoeba-table title='Pending Job' textClass='text-danger' :parentItems="pendingJob"></amoeba-table>
        <base-button title='test'> </base-button>
    </div>
</template>

<script>
import HeaderNav from '../layouts/HeaderNav.vue'
import AmoebaTable from '../components/AmoebaTable.vue'
import BaseButton from '../components/BaseButton.vue'

export default {
name: 'HomePage',
  components: { 
    HeaderNav ,
    AmoebaTable,
    BaseButton
  }, data() {
      return {
        runningJob: [
          { job_id: 1, job_name: 'Test 1', status: 'R' },
          { job_id: 2, job_name: 'Test 2', status: 'R' },
          { job_id: 3, job_name: 'Test 3', status: 'R' },
          { job_id: 4, job_name: 'Test 4', status: 'R' }
        ],
        pendingJob: [
          { job_id: 5, job_name: 'Test 5', status: 'P' },
          { job_id: 6, job_name: 'Test 6', status: 'P' },
          { job_id: 7, job_name: 'Test 7', status: 'P' },
          { job_id: 8, job_name: 'Test 8', status: 'P' }
        ]
      }
    }
  
}
</script>



