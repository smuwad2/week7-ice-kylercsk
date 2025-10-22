<script>
    export default { 
        // Add code in appropriate places
        data() {
            return {
                items: ['keyboard', 'mouse', 'iPhone', 'macbook', 'adapter'],
                test:""
            }
            
        },
        methods:{
            addItem(){
                this.items.push(this.test)
            }
        }
    }
</script>

<template>

    <h2>Shopping Cart</h2>
    <!-- TODO: Add Code Here -->
     <ul>
        <li v-for='(item,index) in items'>{{ item }} <button @click="this.items.splice(index,1)">Delete!</button></li> 
     </ul>
     <input type='text' v-model="test"></input><button @click="addItem()">Add</button>
   
</template>
