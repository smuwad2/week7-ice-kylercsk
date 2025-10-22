<script>
import { computed } from 'vue';

    export default { 
        // Add Code Here to complete the task
        data(){
            return{
                operators:['+','-','*','/','%'],
                x:0,
                y:0,
                selectedOp:'',
            }
        },
        computed:{
            result()
            {
                if(this.selectedOp=='+'){
                    return this.x+this.y
                }
                if(this.selectedOp=='-'){
                    return this.x-this.y
                }
                if(this.selectedOp=='*'){
                    return this.x*this.y
                }
                if(this.selectedOp=='/'){
                    return this.x/this.y
                }
                if(this.selectedOp=='%'){
                    return this.x%this.y
                }
            }
            }
        }
        // Note: DO NOT USE "eval()". In security, "eval" is considered "evil"!!!

</script>

<template>
    <p>x <input v-model.number="x"></p>
    <select v-model="selectedOp">
        <option v-for="op in operators" >{{ op }}</option>
    </select>
    <p>y <input v-model.number="y"></p>
    
    <p>---------------------</p>

    <p>= {{result}}</p>
</template>

<style scoped>
    p, input { font-family: monospace; }
    p { white-space: pre; }

</style>
