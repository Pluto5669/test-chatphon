<template>
    <div>
        <h1>เเสดงข้อมูลนักศึกษา</h1>
        <ul>
            <li v-for="st in student" :key="st.code">
                <span> {{ st.code }} </span>
                <span> {{ st.username }} </span>
                <span> {{ st.password }} </span>
            </li>
        </ul>
    </div>
</template>

<script>
import axios from 'axios'
export default {
    data: () => ({
        student:[
            {id:'001', username:'Pluto_0 ', password:' 123456'},
            {id:'002', username:'Pluto_1 ', password:' 123456'},
            {id:'003', username:'Pluto_2 ', password:' 123456'},
            {id:'004', username:'Pluto_3 ', password:' 123456'},
            {id:'005', username:'Pluto_4 ', password:' 123456'},
        ]
    }),
    async created() {
        const response = await axios.get('http://localhost:7000/list')
        const data = response.data
        this.student = data.row
        console.log(data)
    }
 }
</script>