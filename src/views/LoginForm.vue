<template>
    <div class="container">

       <TheForm 
       :inputs="inputs" 
       :selects="selects"/>
        
        </div>
</template>
<script>

import TheForm from '../components/TheForm.vue';
export default {
    name: 'LoginForm',
    components: {  TheForm },
    data: function(){
        return{

            inputs: [
                [   {
                    theType:'text',  
                    id:'first-name', 
                    label:'User Name',  
                    theClass:'form-control', 
                    theVal: '',
                    placeholder: 'First Name'
                    }
                ],
                [
                    {
                    theType:'text',  
                    id:'last-name', 
                    label:'User Last',  
                    theClass:'form-control', 
                    theVal: '',
                    placeholder: 'Last Name'

                    }
                ],
                [
                    {
                    theType:'email',  
                    id:'e-mail', 
                    label:'E-mail',  
                    theClass:'form-control', 
                    theVal: '',
                    placeholder: 'example@company.com'

                    }
                ],
                 [
                    {
                    theType:'tel',  
                    id:'the-telephone', 
                    label:'Telephone',  
                    theClass:'form-control', 
                    theVal: '',
                    placeholder: '(555) 555-5555'

                    }
                ],
        ],
        selects: [{X:'HOLE'}],
        textAreas: [],
        buttons: []
    }
    }
}
</script>