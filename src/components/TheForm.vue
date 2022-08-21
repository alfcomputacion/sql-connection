<template>
<div class="container">
    <div class="form">
        <h1>LOG IN</h1>
        <div v-if="selects" class="selects">
            <h1>SELECTS go here</h1>
            <BaseSelect
            id="select-number" 
            class="col"
            :options="selects"
            label="Select One"/>

        </div>
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
        <div v-if="textAreas" class="text-areas">
            <h1>TEXT AREAS go here</h1>
            <BaseTextArea 
            :label="textAreas[0].label"
            />
        

        </div>
        <div v-if="radioButtons" class="radio-buttons">
            <h1>BUTTONS go here</h1>
        </div>
        <div v-if="radios" class="selects">
            <h1>RADIO BUTTONS go here</h1>
        </div>
        <div v-if="checks" class="selects">
            <h1>CHECK BOXES go here</h1>
        </div>
        <BaseRadioButton 
            v-for="radio in radioButtons" 
            :key="radio"
            :type="radio[0].type" 
            :name="radio[0].name" 
            :id="radio[0].id" 
            :label="radio[0].label" />
            <!-- <BaseRadioButton type="radio" name="rad" id="radio-button" label="rb1"/>
            <BaseRadioButton type="radio" name="rad" id="radio-button2" label="rb2"/> -->
    <BaseButton label="Submit" theClass="form-control btn btn-primary"/>
    </div><!--end div form  -->
</div>
    
 
</template>
<script>

import BaseInput from './BaseInput.vue';
import BaseSelect from './BaseSelect.vue';
import BaseTextArea from './BaseTextArea.vue';
import BaseButton from './BaseButton.vue';
import BaseRadioButton from './BaseRadioButton.vue';

export default {
    name: 'TheForm',
    components: { BaseInput, BaseSelect, BaseTextArea, BaseButton, BaseRadioButton },
    data: function(){
        return{
            theInputs: this.inputs,
            
        }
    },
    props: {
        inputs: Array,
        selects: Array,
        textAreas: Array,
        buttons: Array,
        radioButtons: Array
    }
}
</script>