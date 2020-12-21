<template>
  <div>
    <input  :type=item.type
            :name=item.name
            :placeholder=item.placeholder
            v-model="info"
            @blur="getInfo()"
            required>
  </div>
</template>

<script>
export default {
  props: {
    item: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {
      info: '',
    };
  },
  methods: {
    getInfo() {
      if (this.item.type === 'text') {
        if (this.info) {
          this.$emit('validateInfo', true);
        } else {
          this.$emit('validateInfo', false);
        }
      } else if (!this.info) {
        this.$emit('validateInfo', false);
      } else {
        this.$emit('validateInfo', this.validEmail(this.info));
      }
    },
    validEmail(email) {
      const re = /^(([^<>()[\]\\.,;:\s@"]+(\.[^<>()[\]\\.,;:\s@"]+)*)|(".+"))@((\[[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\.[0-9]{1,3}\])|(([a-zA-Z\-0-9]+\.)+[a-zA-Z]{2,}))$/;
      return re.test(email);
    },
  },
};

</script>

<style lang="scss" scoped>
div{
  input {
    display: block;
    margin-right: auto;
    margin-left: auto;
    margin-bottom: 30px;
    width: 100%;
    border: 1px solid #fff;
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 30px;
    height: 50px;
    font-family: Lato, sans-serif;
    font-size: 24px;
    font-weight: 700;
    color: #282828;
    padding-left: 38px;
    appearance: textfield;
    outline: none;
    &::placeholder {
      color: #282828;
    }
    &::-moz-placeholder {
      opacity: 1;
    }
  }
}
</style>
