<template>
    <!-- User Account: style can be found in dropdown.less -->
      <li class="dropdown user user-menu">
        <a href="#" class="dropdown-toggle" data-toggle="dropdown">
          <img src="~/assets/img/user2-160x160.jpg" class="user-image" alt="User Image">
          <span class="hidden-xs">{{name}}</span>
        </a>
        <ul class="dropdown-menu">
          <!-- User image -->
          <li class="user-header">
            <img src="~/assets/img/user2-160x160.jpg" class="img-circle" alt="User Image">
            <p>
              {{name}}
              <br />
              {{email}}
              <small>{{birthday}}</small>
            </p>
          </li>
         
          <!-- Menu Footer-->
          <li class="user-footer">
            <div class="pull-left">
              <nuxt-link to="/dashboard/profile" class="btn btn-default btn-flat">Mi perfil</nuxt-link>
            </div>
            <div class="pull-right">
                <nuxt-link to="/logout" class="btn btn-default btn-flat"
                onclick="event.preventDefault();
                              document.getElementById('logout-form').submit();">
                 Desconectarse
              </nuxt-link>

             <form id="logout-form" action="logout" method="POST" style="display: none;">
                 
             </form>
            </div>
          </li>
        </ul>
      </li>
</template>

<script>
export default {
    data(){
        return{
            name: 'Alejandro Cayssials',
            email: 'admin@webxander.com',
            birthday: '18/08/1983'
        }
    }
}
</script>