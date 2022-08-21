<template>
    <div class="row">
        <div class="col-6 text-left pl-5 mx-auto">
            <input :type="type" :name="name" :id="id">
            <label class="pl-2" :for="id">{{label}}</label>
            <div class="text-danger">{{error}}</div>
        </div>

    </div>
</template>
<script>
export default {
    name: 'BaseRadioButton',
    props: {
        type: String,
        name: String,
        id: String,
        label: String,
        error: String
    }
}
</script>