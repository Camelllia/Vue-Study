<template>
    <!--[s] ==============비밀번호 컴포넌트==============-->
    <div>
        <input type="password" name="mbrPaswdStr" id="mbrPaswdStr" class="input-a" placeholder="비밀번호" value="" @input="pwChange"/>
    </div>
    <!--[e] ==============비밀번호 컴포넌트==============-->
</template>

<script>
  export default {
    name: 'Pw-Input',
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
        pwChange($event) {
            this.$emit('input', $event.target.value);
        },
    }
  };
</script>