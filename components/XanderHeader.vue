<template>
    <header class="main-header">
  <!-- Logo -->
  <nuxt-link to="/dashboard" class="logo">
    <!-- mini logo for sidebar mini 50x50 pixels -->
    <span class="logo-mini"><b>W</b>S</span>
    <!-- logo for regular state and mobile devices -->
    <span class="logo-lg"><b>Web</b> Sales</span>
  </nuxt-link>
  <!-- Header Navbar: style can be found in header.less -->
  <nav class="navbar navbar-static-top">
    <!-- Sidebar toggle button-->
    <div><a href="#" class="sidebar-toggle" data-toggle="push-menu" role="button">
      <span class="sr-only">Toggle navigation</span>
    </a>
  </div>
  
  <xander-menu />

  <!-- Navbar Right Menu -->
  <div class="navbar-custom-menu">
    
    <ul class="nav navbar-nav">
    
      <xander-notifications />
      <li>
        <nuxt-link to="/dashboard/company">
          <strong>
            <i class="fa fa-building-o"></i>
          {{company}}
          <span class="text-yellow">
            <i class="fa fa-angle-right"></i> 
              {{shop}}
          </span>
          </strong>
        </nuxt-link>
        
      </li>

      <xander-user-account />

      <!-- Control Sidebar Toggle Button -->
      <li>
        <nuxt-link to="#" data-toggle="control-sidebar"><i class="fa fa-gears"></i></nuxt-link>
      </li>
    </ul>
  </div>
</nav>
</header>
</template>

<script>
import XanderMenu from '~/components/XanderMenu.vue'
import XanderUserAccount from '~/components/XanderUserAccount.vue'
import XanderNotifications from '~/components/XanderNotifications.vue'

export default {
    data(){
        return{
            company: 'Mi empresa',
            shop: 'Mi sucursal'
        }
    },
    components: {
      XanderMenu,
      XanderUserAccount,
      XanderNotifications

    }
}
</script>