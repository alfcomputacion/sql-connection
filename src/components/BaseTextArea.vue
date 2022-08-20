<template>
<div class="row">
    <div class="form-group col-12 mx-auto">

        <label :for="id">{{label}}</label>
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