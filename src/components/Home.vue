<template>
    <div>
        <navbar></navbar>
        <div subs="main_body">
            <input type="text" placeholder="Search">
            <div subs="greeting">
                <h1>Welcome back {{name}}!</h1>
            </div>
            <div subs="yoursubs">
                <h1>Your subjs</h1>
                <ul>
                    <li v-for="sub in subjs" :key="sub.index">
                        <h1>{{sub.course}}</h1>
                        <h2>{{sub.type}}</h2>
                        <p>You have accomplished {{sub.status}} of the module. Keep up the good work!</p>
                    </li>
                </ul>
            </div>
        </div>
        <rightbar></rightbar>
    </div>
</template>
<script>
import Navigation from './Navigation'
import RightNav from './RightNav'

export default {
    name: 'Home',
    components:{
        "navbar": Navigation,
        "rightbar": RightNav,
    },
    data(){
        return{
            name:"Juan",
            subjs:[
                {course:"MATH-4",type:"Algebra",status:"80%"},
                {course:"ENG-3",type:"Grammar",status:"80%"},
                {course:"SCI-3",type:"Biology",status:"80%"},
            ],
        }
    }
}
</script>
<style scoped>
.main_body{
    top: 0;
    padding-left: 17%;
    padding-right: 17%;
    background: #eef0ef;
}
.main_body input{
    width: 100%;
}
.greeting{
    width: 100%;
    height: 150px;
    background: #b9e8d4;
    border-radius: 10px;
}
.greeting h1{
    padding: 5% 20% 10%;
    color: #54bca2; 
}
</style>