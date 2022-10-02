<template>
  <div class="description">
    <h2 class="description__title">{{rep.title}}</h2>
    <p>{{rep.description}}</p>
    <div class="buttons">
      <div class="buttons__stars buttons__section">
        <button><img src="icons/Star.svg" class="buttons__icon"><span>Star</span></button>
        <div class="buttons__count">{{rep.stars}}</div>
      </div>
      <div class="buttons__fork buttons__section">
        <button><img src="icons/Fork.svg" class="buttons__icon"><span>Fork</span></button>
        <div class="buttons__count">{{rep.fork}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'RepositoryDescription',
  props: {
    rep: {
      type: Object,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
.description {
  border-radius: 10px;
  border: 1px solid hsla(0, 0%, 95%, 1);
  box-shadow: 0 0 10px 0 hsla(0, 0%, 0%, 0.07);
  width: 100%;
  text-align: left;
  padding: 25px 20px;
  margin-bottom: 20px;
  margin-top: 20px;
  display:flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: flex-start;

  &__title {
    margin: 0 0 20px;
  }
}
.buttons {
  display: flex;
  align-items: center;
  margin-top: 40px;
  border: 1px solid hsla(210, 13%, 12%, 0.15);
  border-radius: 5px;
  &__section {
    display: flex;
    align-items: center;
  }
  button {
    display: flex;
    align-items: center;
    background: #FAFBFC;
    border: none;
    padding: 5px 10px;
    border-right: 1px solid hsla(210, 13%, 12%, 0.15);
  }
  &__stars {
    border-right: 2px solid hsla(210, 13%, 12%, 0.15);
  }
  &__icon {
    margin-right: 5px;
  }
  &__count {
    padding: 5px 10px;
  }
}

</style>
