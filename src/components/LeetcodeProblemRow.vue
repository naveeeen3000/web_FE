<template>
    <tr v-for="problem in data">
        <td>{{ problem.leetcode_question_link.split('/')[4] }}</td>
        <td>{{ problem.difficulty || "NA"}}</td>
        <td>{{ problem.topic }}</td>
        <td>{{ problem.started_at || "Start now" }}</td>
        <td>{{ problem.started_ar || "Not completed yet" }}</td>
    </tr>
    
</template>

<script>
export default{
    data(){
        return {
            data: null,
        }
    },
    async mounted(){
        const baseUrl = import.meta.env.VITE_API_BASE_URL;
        const endpoint = "leetcode/problems";
        const url = baseUrl + endpoint;
        const res = await fetch(url + '?' + new URLSearchParams({
            limit: 10
        }),{
            method: "GET",
            headers: {
                "Content-Type": "application/json"
            }
        });
        if (res.status == 200){
            this.data = await res.json();
            console.log(res);
        }
    }
}
</script>