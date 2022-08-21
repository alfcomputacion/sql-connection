<template>
    <div class="row">
        <div class="col-6 text-center p-4 mx-auto">
        <button 
            :class="theClass">
            {{label}}
        </button>
        
        </div>
    </div>
</template>

<script>
export default {
    name: 'BaseButton',
    props: {
        theClass: String,
        label: String
    }
}
</script>