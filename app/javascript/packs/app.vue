<template>
  <div id="app">
    <p>{{ message }}</p>

    <div class="block">
      <a class="button">Button</a>
      <a class="button is-white">White</a>
      <a class="button is-light">Light</a>
      <a class="button is-dark">Dark</a>
      <a class="button is-black">Black</a>
      <a class="button is-link">Link</a>
    </div>
    <div class="block">
      <a class="button is-primary">Primary</a>
      <a class="button is-info">Info</a>
      <a class="button is-success">Success</a>
      <a class="button is-warning">Warning</a>
      <a class="button is-danger">Danger</a>
    </div>


      <b-dropdown>
        <button class="button" slot="trigger">
            <span>Dropdown</span>
            <b-icon icon="arrow_drop_down"></b-icon>
        </button>

        <b-dropdown-option>Action</b-dropdown-option>
        <b-dropdown-option>Another action</b-dropdown-option>
        <b-dropdown-option>Something else</b-dropdown-option>
    </b-dropdown>

    <b-dropdown disabled>
        <button class="button" slot="trigger">
            <span>Dropdown</span>
            <b-icon icon="arrow_drop_down"></b-icon>
        </button>

        <b-dropdown-option>Action</b-dropdown-option>
        <b-dropdown-option>Another action</b-dropdown-option>
        <b-dropdown-option>Something else</b-dropdown-option>
    </b-dropdown>


    <div class="block">
        <b-radio-group v-model="radio">
            <b-radio value="Flint">Flint</b-radio>
            <b-radio value="Silver">Silver</b-radio>
            <b-radio value="Jack">Jack</b-radio>
            <b-radio value="Vane" disabled>Vane</b-radio>
        </b-radio-group>
    </div>
    <p class="content"><b>Selection:</b> {{ radio }}</p>

    <h3 class="subtitle">Vertical example</h3>
    <b-radio-group v-model="radio">
        <div class="field">
            <b-radio value="Flint">Flint</b-radio>
        </div>
        <div class="field">
            <b-radio value="Silver">Silver</b-radio>
        </div>
        <div class="field">
            <b-radio value="Jack">Jack</b-radio>
        </div>
        <div class="field">
            <b-radio value="Vane" disabled>Vane</b-radio>
        </div>
    </b-radio-group>



    <div class="block">
    <b-switch>Default</b-switch>
    <b-switch v-model="isSwitched">{{ isSwitched }}</b-switch>
    <b-switch disabled>Disabled</b-switch>
    <b-switch disabled checked>Disabled Checked</b-switch>
</div>

<h3 class="subtitle">Vertical example</h3>
<div class="block">
    <div class="field">
        <b-switch>Default</b-switch>
    </div>
    <div class="field">
        <b-switch v-model="isSwitched">{{ isSwitched }}</b-switch>
    </div>
    <div class="field">
        <b-switch disabled>Disabled</b-switch>
    </div>
    <div class="field">
        <b-switch disabled checked>Disabled Checked</b-switch>
    </div>
</div>

  </div>
</template>

<script>
export default {
  data: function () {
    return {
      message: "Hello Vue!"
    }
  }
}
</script>

<style lang="scss">
  // Import Bulma's core
  @import "~bulma/sass/utilities/_all";

  // Set your colors
  $primary: #f1896f;
  $primary-invert: findColorInvert($primary);
  $twitter: #4099ff;
  $twitter-invert: findColorInvert($twitter);

  // Setup $colors to use as bulma classes (e.g. 'is-twitter')
  $colors: (
      "white": ($white, $black),
      "black": ($black, $white),
      "light": ($light, $light-invert),
      "dark": ($dark, $dark-invert),
      "primary": ($primary, $primary-invert),
      "info": ($info, $info-invert),
      "success": ($success, $success-invert),
      "warning": ($warning, $warning-invert),
      "danger": ($danger, $danger-invert),
      "twitter": ($twitter, $twitter-invert)
  );

  // Links
  $link: $primary;
  $link-invert: $primary-invert;
  $link-focus-border: $primary;

  // Import Bulma and Buefy styles
  @import "~bulma";
  @import "~buefy/src/scss/buefy";
</style>
