<template>
    <div id="app">
        <li v-for="item in items" :key="item.name" id="itemsList">
            <h1>{{ item.name }}</h1>
        </li>
    </div>
</template>

<script>
    document.getElementById("app").style.minHeight = document.body.clientWidth;
    
    export default {
        data() {
            return {
               items:[
                    {name: "Max"},
                    {name: "Liam2"},
                    {name: "Maxs"},
                    {name: "Liam"},
                    {name: "Max2"},
                    {name: "Liam6"},
                    {name: "Max3"},
                    {name: "Liam3"},
                    {name: "Max5"},
                    {name: "Liam5"},
                    {name: "Max33"},
                    {name: "Liam33"},
                    {name: "Max53"},
                    {name: "Liam53"}
                    
               ]
            }
        },
    }
</script>

<style scoped>
#itemsList{
    overflow:hidden; overflow-y:scroll;
}
li{
    list-style-type: none;
    width: 100%;
    color: rgb(0, 0, 0);
    min-height: 50px;
    background-color: rgb(188, 205, 240);
    border-bottom: 1px solid rgb(255, 255, 255);
   
   
}
</style>