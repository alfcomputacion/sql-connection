<template>
<div class="container">
    <div class="row col-6 mx-auto form-group">
        <label :for="id">{{label}}</label>
    <input 
        :type="theType" 
        :id="id" 
        :class="theClass"
        :value="theVal"
        :placeholder="placeholder">
    </div>
</div>
</template>

<script>
export default {
    name: 'BaseInput',
    props: {
        id: String,
        theClass: String,
        label: String,
        theType: String,
        theVal: String,
        placeholder: String
    }
}
</script>