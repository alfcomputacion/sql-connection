<template>
<div class="container">
    <div class="form">
        <h1>LOG IN</h1>
        <div v-if="inputs" class="inputs">
        <BaseInput 
            v-for="input in inputs" 
            :key="input"
            :id="input[0].id"   
            :theClass="input[0].theClass"   
            :label="input[0].label"   
            :theType="input[0].theType" 
            :theVal="input[0].theVal"
            :placeholder="input[0].placeholder"  />
        </div>
        <div v-if="selects" class="selects">
            <h1>SELECTS go here</h1>
            <BaseSelect 
            :options="selects"
            label="Select One"/>

        </div>
        <div v-if="textAreas" class="selects">
            <h1>TEXT AREAS go here</h1>
        </div>
        <div v-if="buttons" class="selects">
            <h1>BUTTONS go here</h1>
        </div>
        <div v-if="radios" class="selects">
            <h1>RADIO BUTTONS go here</h1>
        </div>
        <div v-if="checks" class="selects">
            <h1>CHECK BOXES go here</h1>
        </div>

    </div><!--end div form  -->
</div>
    
 
</template>
<script>

import BaseInput from './BaseInput.vue';
import BaseSelect from './BaseSelect.vue';
export default {
    name: 'TheForm',
    components: { BaseInput, BaseSelect },
    data: function(){
        return{
            theInputs: this.inputs
        }
    },
    props: {
        inputs: Array,
        selects: Array,
        textAreas: Array,
        buttons: Array
    }
}
</script>