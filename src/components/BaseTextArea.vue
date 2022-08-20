<template>
<div class="row">
    <div class="form-group col-6 mx-auto">
        <label class="float-left ml-3" :for="id">{{label}}</label>
        <textarea 
        :name="name" 
        :id="id" 
        :cols="cols" 
        :rows="rows">
        </textarea>
    </div>
</div>
</template>

<script>
export default {
    name: 'BaseTextArea',
    props: {
        label: String,
        name: String,
        id: String,
        cols: Number,
        rows: Number,
        theClass: String
    }
}
</script>
<style scoped>
    textarea{
 
        width: 95%;
        border-radius: 7px;
    }

</style>