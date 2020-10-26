<template>
    <div class="rightnav">
        <div class="profile">
            <h1>{{name}}</h1>
            <p>{{status}}</p>
        </div>
        <h3>Reminders</h3>
        <div class="reminders">
            <ul>
                <li v-for="reminder in reminders" :key="reminder.index">
                    <h2>{{reminder.course}} - {{reminder.notification}}</h2>
                    <p>{{reminder.date}}</p>
                </li>
            </ul>
        </div>
    </div>
</template>
<script>
export default {
    name: 'RightNav',
    data(){
        return{
          name:"Juan Dela Cruz",
          status:"Student",
          reminders:[
              {course:"Biology", notification:"Send homework", date:"28 Dec 2020, Friday"},
              {course:"Algebra", notification:"Send homework", date:"28 Dec 2020, Friday"},
              {course:"Grammar", notification:"Send homework", date:"28 Dec 2020, Friday"},
          ],
        }
    },
}
</script>
<style>
body {font-family: Arial, Helvetica, sans-serif;}
.rightnav {
  height: 100%;
  width: 15%;
  position: fixed;
  z-index: 1;
  top: 0;
  background-color: #fbf9fa;
  overflow-x: hidden;
  padding-top: 20px;
  float: right;
  right:0;
}

.rightnav .profile{
    padding: 10px 10px 10px;
    background-color:#eef0ef;
    border-radius: 10 px;
    display: block;
}

.profile h1{
    padding: 6px 8px 1px 16px;
    font-size: 18px;
    color: #111;
}

.profile p{
    padding: 6px 8px 1px 16px;
    font-size: 14px;
    color: #dad4dc;   
}

.rightnav a {
  padding: 6px 8px 6px 16px;
  text-decoration: none;
  font-size: 18px;
  color: #dad4dc;
  display: block;
}

.rightnav a:hover {
  color: #111;
}

.rightnav a.logout{
  margin-top: 200%;
}

.main {
  margin-left: 160px;
  font-size: 28px; 
  padding: 0px 10px;
}

</style>