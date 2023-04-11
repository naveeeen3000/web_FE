<template>
<div class="container">
  <h2>Leet code problems</h2>
  <table>
    <thead>
      <tr>
        <td>Problem</td>
        <td>Difficulty</td>
        <td>Topic</td>
        <td>Status</td>
        <td>Completed at</td>
      </tr>
    </thead>
    <tbody>
      <LeetcodeProblemRow />
    </tbody>
  </table>
</div>
</template>
<style>
.container{
  color: black;
  font-size: large;
}
table{
  border: 5px solid black;
  /* display: block; */
}
tr{
  /* display: flex; */
  /* justify-content: space-around; */
}
thead{
  background-color: black;
  color: var(--blue);
  font-weight: bold;
  /* display: block; */
}
tbody{
  /* display: table; */
}
</style>

<script>
import LeetcodeProblemRow from './LeetcodeProblemRow.vue';
export default{
  data(){
    return {
      
    }
  },
  components:{
    LeetcodeProblemRow,
  }
}
</script>