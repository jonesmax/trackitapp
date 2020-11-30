<template>
    <div id="app">
        <div id="content">
            <h1>{{day}}</h1>
            <h1>{{time}}</h1>
        </div>
    </div>
</template>

<script>
    export default {
        data() {
            return {
               time: 0,
               day: 0
            }
        },
        methods:{
            getNow(){
                const today = new Date();
                //time
                var hour = today.getHours();
                var minute = today.getMinutes();
                var ampm = " am";
                if(hour>12){
                    hour-=12;
                    ampm=" pm"
                }
                if(minute<10){
                    minute = "0"+minute;
                }
                this.time = hour+":"+minute+ampm;  
                //day
                var day = today.getDay();
                var weekday = new Array(7);
                weekday[0] = "Sunday";
                weekday[1] = "Monday";
                weekday[2] = "Tuesday";
                weekday[3] = "Wednesday";
                weekday[4] = "Thursday";
                weekday[5] = "Friday";
                weekday[6] = "Saturday";

                var month = today.getMonth();
                var months = new Array(12);
                months[0] = "January";
                months[1] = "February";
                months[2] = "March";
                months[3] = "April";
                months[4] = "May";
                months[5] = "June";
                months[6] = "July";
                months[7] = "August";
                months[8] = "September";
                months[9] = "October";
                months[10] = "November";
                months[11] = "December";

                this.day=weekday[day]+", "+months[month]+" "+today.getDate();
            }

        },
        created() {
          this.interval = setInterval(() => this.getNow(), 1000);
        }
       
    }
</script>

<style>
#content{
    padding: 4%;
    font-size: 85%;
    color: white;
    
}
</style>