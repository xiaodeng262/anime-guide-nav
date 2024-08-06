<template>
  <div class="home">
    <el-container class="full-height">
      <el-aside width="250px" class="desktop-aside">
        <div class="sidebar-content">
          <div class="logo-container">
            <img src="http://www.animeguide.top:8091/themes/theme-heolink/assets/images/logo_cover.jpg" alt="Logo"
                 class="logo-image">
          </div>
          <el-menu
              default-active="2"
              class="el-menu-vertical-demo"
              background-color="#545c64"
              text-color="#fff"
              active-text-color="#ffd04b">
            <el-menu-item index="1" @click="scrollTo('section1')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
            <el-menu-item index="2" @click="scrollTo('section2')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
            <el-menu-item index="3" @click="scrollTo('section3')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
            <el-menu-item index="4" @click="scrollTo('section4')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
            <el-menu-item index="5" @click="scrollTo('section5')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
            <el-menu-item index="6" @click="scrollTo('section6')">
              <i class="el-icon-menu"></i>
              <span slot="title">导航1</span>
            </el-menu-item>
          </el-menu>
        </div>
      </el-aside>
      <el-container class="main-container">
        <el-header class="mobile-header">
          <img src="http://www.animeguide.top:8091/themes/theme-heolink/assets/images/logo_cover.jpg" alt="Logo"
               class="mobile-logo">
          <el-button @click="drawerVisible = true" icon="el-icon-menu" class="mobile-menu-button"></el-button>
        </el-header>
        <el-main>
          <el-card class="hero-card">
            <h1 class="hero-title">Welcome to Our Site</h1>
            <p class="hero-subtitle">Discover amazing content and features</p>
          </el-card>
          <el-card>
            <div id="section1">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <div id="section2">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <div id="section3">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <div id="section4">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <div id="section5">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <div id="section6">
              <h3>xxxxx</h3>
              <div>
                <ul>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                  <li>11313123</li>
                </ul>
              </div>
            </div>
            <!-- Repeat for other sections -->
          </el-card>
        </el-main>
      </el-container>
    </el-container>
    <el-drawer
        title="菜单"
        :visible.sync="drawerVisible"
        direction="ltr"
        size="80%">
      <el-menu
          default-active="2"
          active-text-color="#ffd04b">
        <el-menu-item index="1" @click="scrollTo('section1')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
        <el-menu-item index="2" @click="scrollTo('section2')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
        <el-menu-item index="3" @click="scrollTo('section3')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
        <el-menu-item index="4" @click="scrollTo('section4')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
        <el-menu-item index="5" @click="scrollTo('section5')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
        <el-menu-item index="6" @click="scrollTo('section6')">
          <i class="el-icon-menu"></i>
          <span slot="title">导航1</span>
        </el-menu-item>
      </el-menu>
    </el-drawer>
  </div>
</template>

<script>
export default {
  name: 'Home',
  data() {
    return {
      drawerVisible: false
    }
  },
  methods: {
    scrollTo(sectionId) {
      const element = document.getElementById(sectionId);
      if (element) {
        element.scrollIntoView({behavior: 'smooth'});
      }
      this.drawerVisible = false;
    }
  }
}
</script>

<style scoped>
.home {
  display: flex;
  background-color: #f0f0f0;
  min-height: 100vh;
}

.full-height {
  min-height: 100vh;
  display: flex;
}

.desktop-aside {
  background-color: #545c64;
  display: flex;
  flex-direction: column;
  height: 100vh;
  position: sticky;
  top: 0;
}

.sidebar-content {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.logo-container {
  padding: 20px;
  background-color: #4a4f57;
}

.logo-image {
  width: 100%;
  max-width: 200px;
  height: auto;
}

.el-menu-vertical-demo {
  flex-grow: 1;
  border-right: none;
}

.main-container {
  flex-grow: 1;
  display: flex;
  flex-direction: column;
}

.hero-card {
  height: 30vh;
  background-image: url('http://www.animeguide.top:8091/themes/theme-heolink/assets/images/index_cover2.jpg');
  background-size: cover;
  background-position: center;
  margin-bottom: 20px;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  color: white;
  text-align: center;
}

.mobile-header {
  display: none;
  align-items: center;
  justify-content: space-between;
  padding: 10px;
  background-color: #545c64;
}

.mobile-logo {
  height: 40px;
}

.mobile-menu-button {
  background: none;
  border: none;
  color: white;
  font-size: 20px;
}

@media (max-width: 768px) {
  .desktop-aside {
    display: none;
  }

  .mobile-header {
    display: flex;
  }

  .el-main {
    padding: 10px;
  }

  .hero-card {
    height: 25vh;
  }

  .hero-title {
    font-size: 1.5em;
  }

  .hero-subtitle {
    font-size: 1em;
  }
}
</style>
