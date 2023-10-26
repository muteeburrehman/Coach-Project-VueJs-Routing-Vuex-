<template>
  <section>
    <base-card>
      <h2>Register as a coach now!</h2>
      <coach-form @save-data="saveData"></coach-form>
    </base-card>
  </section>
</template>

<script>
import CoachForm from '../../components/coaches/CoachForm.vue';

export default {
  components: {
    CoachForm,
  },

  methods:{
    saveData(data){
       this.$store.dispatch('coaches/registerCoach',data);
       this.$router.replace('/coaches');//We can also use push here, but push take us back to previous page i.e form page in this case

    }
  }
};
</script>