<template>
  <v-footer
    color="primary"
    dark
    app
    absolute
  >
    <v-container
      fluid
    >
      <v-row
        no-gutters
      >
        <v-col
          cols="12"
          md="4"
          xs="12"
        >
          <v-row :justify="$vuetify.breakpoint.mdAndUp ? 'left' : 'center'">
            <h3>
              {{ $t('footer.title') }}
            </h3>
          </v-row>
        </v-col>
        <v-col
          cols="12"
          md="4"
          xs="12"
        >
          <v-row justify="center">
            <a
              class="footer-link"
              target="_blank"
              href="https://www.netlify.com"
            >
              {{ $t('footer.netlify') }}
            </a>
          </v-row>
        </v-col>
        <v-col
          cols="12"
          md="4"
          xs="12"
        >
          <v-row justify="center">
            <v-spacer v-if="$vuetify.breakpoint.mdAndUp" />
            <social-button
              dark
              x-large
              :link="github"
            >
              <i
                class="fab fa-github-alt"
              />
            </social-button>
            <social-button
              dark
              x-large
              :link="twitter"
            >
              <i class="fab fa-twitter" />
            </social-button>
            <social-button
              dark
              x-large
              :link="instagram"
            >
              <i class="fab fa-instagram" />
            </social-button>
            <social-button
              dark
              x-large
              :link="facebook"
            >
              <i class="fab fa-facebook-f" />
            </social-button>
          </v-row>
        </v-col>
      </v-row>
    </v-container>
  </v-footer>
</template>

<script>
import SocialButton from '@/components/buttons/SocialButton.vue';

export default {
  components: {
    SocialButton,
  },
  data: () => ({
    twitter: 'https://twitter.com/speakherjapan',
    facebook: 'https://www.facebook.com/speakherjp',
    instagram: 'https://www.instagram.com/speakherjp/',
    github: 'https://github.com/WWCodeTokyo/speak-her-db',
  }),
};
</script>
