<script>
    export default { 
        data() {
            return {
                // Add code here
                isRed: false,
                isRedbtn: false,
                id: 'demo1'
            }
        },
        methods: {
   			// Add code here
            toggleColor() {
                this.isRed = !this.isRed;
                this.isRedbtn = !this.isRedbtn;
            }
		}
    }
</script>


<template>
    
    <!-- Modify code here -->
    <div class="container">
        <div v-bind:id="id" class="m-2" v-bind:class="isRed ? 'redBox' : 'blueBox'">
            div ID : {{id}} 
        </div>
        
        <button type="button" v-on:click="toggleColor" v-bind:class="isRedbtn ? 'btn-danger' : 'btn-secondary'" :class="btn">Change Color</button>
    </div>

</template>

<style scoped>
    .redBox {
        background-color: red;
    }
    .blueBox {
        background-color: blue;
    }
    #demo1 {
        color: white;
    }
</style>
