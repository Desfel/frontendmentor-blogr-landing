<template>
  <section class="page-wrapper">
    <section class="header-section">
      <div class="navigation-wrapper">
        <div class="left-nav">
          <a href="#" class="logo">
            <img src="@/assets/img/logo.svg" alt="Blogr" />
          </a>

          <nav>
            <div class="parent-link-wrapper">
              <a href="#" class="parent-link">
                <span>Product</span>
                <img src="@/assets/img/icon-arrow-light.svg" alt="Arrow" />
              </a>
              <div class="subnav-menu-wrapper">
                <div class="subnav-menu">
                  <a href="#">Overview</a>
                  <a href="#">Pricing</a>
                  <a href="#">Marketplace</a>
                  <a href="#">Features</a>
                  <a href="#">Integrations</a>
                </div>
              </div>
            </div>

            <div class="parent-link-wrapper">
              <a href="#" class="parent-link">
                <span>Company</span>
                <img src="@/assets/img/icon-arrow-light.svg" alt="Arrow" />
              </a>

              <div class="subnav-menu-wrapper">
                <div class="subnav-menu">
                  <a href="#">About</a>
                  <a href="#">Team</a>
                  <a href="#">Blog</a>
                  <a href="#">Careers</a>
                </div>
              </div>
            </div>

            <div class="parent-link-wrapper">
              <a href="#" class="parent-link">
                <span>Connect</span>
                <img src="@/assets/img/icon-arrow-light.svg" alt="Arrow" />
              </a>

              <div class="subnav-menu-wrapper">
                <div class="subnav-menu">
                  <a href="#">Contact</a>
                  <a href="#">Newsletter</a>
                  <a href="#">LinkedIn</a>
                </div>
              </div>
            </div>
          </nav>
        </div>

        <div class="right-nav">
          <div class="desktop-nav">
            <a href="#" class="site-btn login-btn">Login</a>
            <a href="#" class="site-btn full-btn">Sign up</a>
          </div>

          <div class="mobile-nav">
            <span class="burger-icon-holder" @click="openBurger" :class="{'is-active': isActive}"></span>
          </div>
        </div>
      </div>

      <div class="header-content">
        <h1>A modern publishing platform</h1>
        <p>Grow your audience and build your online brand</p>

        <div class="header-button-wrapper">
          <a href="#" class="site-btn full-btn">Start for Free</a>
          <a href="#" class="site-btn outlined-btn">Learn More</a>
        </div>
      </div>
    </section>

    <section class="intro-section">
      <h2>Designed for the future</h2>

      <div class="intro-content-wrapper">
        <div class="left-intro-content">
          <div class="intro-content">
            <h3>Introducing an extensible editor</h3>
            <p>
              Blogr features an exceedingly intuitive interface which lets you focus on one thing:
              creating content. The editor supports management of multiple blogs and allows easy
              manipulation of embeds such as images, videos, and Markdown. Extensibility with plugins and
              themes provide easy ways to add functionality or change the looks of a blog.
            </p>
          </div>

          <div class="intro-content">
            <h3>Robust content management</h3>
            <p>
              Flexible content management enables users to easily move through posts.
              Increase the usability of your blog by adding customized categories, sections,
              format, or flow. With this functionality, you’re in full control.
            </p>
          </div>
        </div>

        <div class="right-intro-content">
          <img class="desktop-img" src="@/assets/img/illustration-editor-desktop.svg" alt="Editor" />
          <img class="mobile-img" src="@/assets/img/illustration-editor-mobile.svg" alt="Editor" />
        </div>
      </div>
    </section>

    <section class="state-section">
      <div class="state-img">
        <img src="@/assets/img/illustration-phones.svg" alt="Phones" />
      </div>

      <div class="state-content">
        <h2>State of the Art Infrastructure</h2>

        <p>
          With reliability and speed in mind, worldwide data centers provide the backbone for ultra-fast
          connectivity. This ensures your site will load instantly, no matter where your readers are,
          keeping your site competitive.
        </p>
      </div>
    </section>

    <section class="second-intro">
      <div class="second-intro-content-wrapper">

        <div class="left-intro-content">
          <img class="desktop-img" src="@/assets/img/illustration-laptop-desktop.svg" alt="Laptop" />
          <img class="mobile-img" src="@/assets/img/illustration-laptop-mobile.svg" alt="Laptop" />
        </div>

        <div class="right-intro-content">
          <div class="intro-content">
            <h3>Introducing an extensible editor</h3>
            <p>
              Blogr features an exceedingly intuitive interface which lets you focus on one thing:
              creating content. The editor supports management of multiple blogs and allows easy
              manipulation of embeds such as images, videos, and Markdown. Extensibility with plugins and
              themes provide easy ways to add functionality or change the looks of a blog.
            </p>
          </div>

          <div class="intro-content">
            <h3>Robust content management</h3>
            <p>
              Flexible content management enables users to easily move through posts.
              Increase the usability of your blog by adding customized categories, sections,
              format, or flow. With this functionality, you’re in full control.
            </p>
          </div>
        </div>
      </div>
    </section>

    <section class="footer-section">
      <a href="#" class="logo">
        <img src="@/assets/img/logo.svg" alt="Blogr" />
      </a>

      <nav class="footer-nav">
        <p class="footer-nav-title">Product</p>

        <p><a href="#">Overview</a></p>
        <p><a href="#">Pricing</a></p>
        <p><a href="#">Marketplace</a></p>
        <p><a href="#">Features</a></p>
        <p><a href="#">Integrations</a></p>
      </nav>

      <nav class="footer-nav">
        <p class="footer-nav-title">Company</p>

        <p><a href="#">About</a></p>
        <p><a href="#">Team</a></p>
        <p><a href="#">Blog</a></p>
        <p><a href="#">Careers</a></p>
      </nav>

      <nav class="footer-nav">
        <p class="footer-nav-title">Connect</p>

        <p><a href="#">Contact</a></p>
        <p><a href="#">Newsletter</a></p>
        <p><a href="#">LinkedIn</a></p>
      </nav>
    </section>

    <div class="mobile-menu-popup" :class="{'is-active': isActive}">
      <div class="mobile-nav-menu">
        <a href="#" class="parent-link"  @click="toggleSubmenu1">
          <span>Product</span>
          <img src="@/assets/img/icon-arrow-dark.svg" alt="Arrow" />
        </a>

        <transition name="slide">
          <nav v-if="subMenuActive1">
            <p><a href="#">Overview</a></p>
            <p><a href="#">Pricing</a></p>
            <p><a href="#">Marketplace</a></p>
            <p><a href="#">Features</a></p>
            <p><a href="#">Integrations</a></p>
          </nav>
        </transition>
      </div>

      <div class="mobile-nav-menu">
        <a href="#" class="parent-link" @click="toggleSubmenu2">
          <span>Company</span>
          <img src="@/assets/img/icon-arrow-dark.svg" alt="Arrow" />
        </a>

        <transition name="slide">
          <nav v-if="subMenuActive2">
            <p><a href="#">About</a></p>
            <p><a href="#">Team</a></p>
            <p><a href="#">Blog</a></p>
            <p><a href="#">Careers</a></p>
          </nav>
        </transition>
      </div>

      <div class="mobile-nav-menu">

        <a href="#" class="parent-link" @click="toggleSubmenu3">
          <span>Connect</span>
          <img src="@/assets/img/icon-arrow-dark.svg" alt="Arrow" />
        </a>


        <transition name="slide">
          <nav v-if="subMenuActive3">
            <p><a href="#">Contact</a></p>
            <p><a href="#">Newsletter</a></p>
            <p><a href="#">LinkedIn</a></p>
          </nav>
        </transition>
      </div>

      <div class="login-menu">
        <a href="#" class="site-btn login-btn">Login</a>
        <a href="#" class="site-btn full-inverted-btn">Sign up</a>
      </div>
    </div>
  </section>
</template>

<script>
import { mapState } from 'vuex'

export default {
  data() {
    return {
      isActive: false,
      subMenuActive1: false,
      subMenuActive2: false,
      subMenuActive3: false
    }
  },
  head() {
    return {
      title: {
        inner: 'Home'
      },
      meta: [
        {
          name: 'description',
          content: `${this.appTitle} home page`,
          id: 'desc'
        }
      ]
    }
  },
  methods: {
    openBurger(e) {
      e.preventDefault()
      this.isActive = !this.isActive;
    },
    toggleSubmenu1(e) {
      e.preventDefault()
      this.subMenuActive1 = !this.subMenuActive1;
      this.subMenuActive2 = false;
      this.subMenuActive3 = false;
    },
    toggleSubmenu2(e) {
      e.preventDefault()
      this.subMenuActive2 = !this.subMenuActive2;
      this.subMenuActive1 = false;
      this.subMenuActive3 = false;
    },
    toggleSubmenu3(e) {
      e.preventDefault()
      this.subMenuActive3 = !this.subMenuActive3;
      this.subMenuActive2 = false;
      this.subMenuActive1 = false;
    }
  },
  computed: mapState('app', ['appTitle'])
}
</script>

<style lang="scss" scoped>
@import '@/theme/variables.scss';
@import '@/theme/header.scss';
@import '@/theme/intro.scss';
@import '@/theme/state.scss';
@import '@/theme/second-intro.scss';
@import '@/theme/footer.scss';

.page-wrapper {
  display: flex;
  flex-direction: column;
  justify-content: center;

  .site-btn {
    display: inline-block;
    padding: 15px 16px;
    border-radius: 28px;
    font-family: $linkFont;
    font-size: 16px;
    line-height: 18px;
    text-align: center;

    @media (min-width: 768px) and (max-width: 1100px) {
      font-size: 14px;
      line-height: 16px;
    }

    &:not(:last-child) {
      margin-right: 16px;

      @media (min-width: 768px) and (max-width: 1100px) {
        margin-right: 10px;
      }
    }

    &.full-btn {
      color: $primaryColor2;
      background: $white;
      transition: all .3s ease-in-out;

      @media (min-width: 1100px) {
        min-width: 137px;
      }

      &:hover {
        color: $white;
        background: $primaryColor2;
      }
    }

    &.full-inverted-btn {
      color: $white;
      background: linear-gradient(135deg, #FF8F71 0%, #FF3E55 100%);
      transition: all .3s ease-in-out;
    }

    &.outlined-btn {
      min-width: 137px;
      border: 1px solid $white;
      color: $white;
      transition: all .3s ease-in-out;

      &:hover {
        color: $primaryColor2;
        background: $white;
      }
    }
  }
}
</style>
