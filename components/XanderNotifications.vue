<template>
    <!-- Notifications: style can be found in dropdown.less -->
      <li class="dropdown notifications-menu">
        <a href="#" class="dropdown-toggle" data-toggle="dropdown">
          <i class="fa fa-bell-o"></i>
          <span class="label label-warning">0</span>
        </a>
        <ul class="dropdown-menu">
          <li class="header">No hay novedades que leer</li>
          <li>
            <!-- inner menu: contains the actual data -->
            <ul class="menu">
              <li>
                <a href="#"> En este momento no tenemos novedades disponibles
                </a>
              </li>
            </ul>
          </li>
          <li class="footer"><a href="#">Ver todas las noticias</a></li>
        </ul>
      </li>
</template>