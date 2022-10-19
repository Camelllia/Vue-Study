<template>
    <!--[s] ==============아이디 컴포넌트==============-->
    <div>
        <input type="text" name="mbrIdStr" id="mbrIdStr" class="input-a" placeholder="아이디" value="" @input="idChange"/>
    </div>
    <!--[e] ==============아이디 컴포넌트==============-->
</template>

<script>
  export default {
    name: 'Id-Input',
    props: {
        value:{

        },
    },
        
    data() {
        return {
            pvalue: this.value
        }
    },

    methods: {
        idChange($event) {
            this.$emit('input', $event.target.value);
        },
    }
  };
</script>