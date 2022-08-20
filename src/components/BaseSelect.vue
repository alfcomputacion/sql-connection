<template>
    <div class="container">
        <label  for="id">{{label}}</label>
        <select 
            :id="id"
            :theClass="theClass"
            :value="theVal"
            @input="$emit('update:modelValue', $event.target.value)">
            <option 
                v-for="option in options" 
                :key="option[1]"
                :value="option[1]" >

                {{option[0]}}
            </option>
        </select>
    </div>
</template>
<script>
export default {
    name: 'BaseSelect',
    data: function(){
        
    },
    props: {
        id: String,
        theClass: String,
        theVal: String,
        options: Array,
        label: String
        
    }
}
</script>
