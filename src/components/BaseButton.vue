<template>
    <div class="row">
        <div class="col-12 text-center p-2">
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