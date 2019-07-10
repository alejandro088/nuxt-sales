<template>
    <!-- Left side column. contains the logo and sidebar -->
<aside class="main-sidebar">
  <!-- sidebar: style can be found in sidebar.less -->
  <section class="sidebar">
    <!-- Sidebar user panel -->
    <div class="user-panel">
      <div class="pull-left image">
        <img src="~/assets/img/user2-160x160.jpg" class="img-circle" alt="User Image">
      </div>
      <div class="pull-left info">
        <p>{{name}}</p>
        <a href="#"><i class="fa fa-circle text-success"></i> Online</a>
      </div>
    </div>
    
    <!-- sidebar menu: : style can be found in sidebar.less -->
    <ul class="sidebar-menu" data-widget="tree">
      <li class="header">MAIN NAVIGATION</li>
      <li class=" treeview menu-open">
        <a href="#">
          <i class="fa fa-dashboard"></i> <span>Dashboard</span>
          <span class="pull-right-container">
            <i class="fa fa-angle-left pull-right"></i>
          </span>
        </a>
        <ul class="treeview-menu">
          <li><nuxt-link to="/dashboard"><i
                class="fa fa-circle-o"></i> Home</nuxt-link></li>
        </ul>
      </li>
      <li class="treeview">
        <a href="#">
          <i class="fa fa-files-o"></i>
          <span>Contabilidad</span>
        </a>
        <ul class="treeview-menu">
          <li >
            <nuxt-link to="/dashboard/reports/cash/daily"><i
                class="fa fa-circle-o"></i> Caja: Movimientos del dia</nuxt-link></li>
          <li >
            <nuxt-link to="/dashboard/reports"><i
                class="fa fa-circle-o"></i> Reportes</nuxt-link></li>
          <li >
            <nuxt-link to="/dashboard/accounts"><i
                class="fa fa-circle-o"></i> Cuentas corrientes</nuxt-link></li>

        </ul>
      </li>
      <li class=" treeview">
        <a href="#">
          <i class="fa fa-files-o"></i>
          <span>Gestion de ventas</span>
        </a>
        <ul class="treeview-menu">
          <li ><nuxt-link to="/dashboard/sales/create"><i
                class="fa fa-circle-o"></i> Nueva venta</nuxt-link></li>
          <li ><nuxt-link to="/dashboard/sales"><i
                class="fa fa-circle-o"></i> Ventas</nuxt-link></li>
          <li ><nuxt-link to="/dashboard/orders"><i
                class="fa fa-circle-o"></i> Pedidos</nuxt-link></li>

        </ul>
      </li>
      <li class="treeview">
        <a href="#">
          <i class="fa fa-files-o"></i>
          <span>Gestion de compras</span>
        </a>
        <ul class="treeview-menu">
          <li ><nuxt-link to="/dashboard/purchases/orders/create"><i class="fa fa-circle-o"></i> Nueva orden de compra</nuxt-link></li>

          <li ><nuxt-link to="/dashboard/purchases/tickets/create"><i class="fa fa-circle-o"></i> Nueva factura de compra</nuxt-link></li>

          <li ><nuxt-link to="/dashboard/purchases/orders"><i class="fa fa-circle-o"></i> Ordenes de compra</nuxt-link></li>

          <li ><nuxt-link to="/dashboard/purchases/tickets"><i class="fa fa-circle-o"></i> Facturas de compra</nuxt-link></li>
        </ul>
      </li>
      <li class="header">CONFIGURATION</li>
      <li >
        <nuxt-link to="/dashboard/settings">
          <i class="fa fa-th"></i> <span>Configuración</span>

        </nuxt-link>
      </li>
      <li >
        <nuxt-link to="/dashboard/employees">
          <i class="fa fa-th"></i> <span>Empleados</span>
          <span class="pull-right-container">
            <small class="label pull-right bg-green">new</small>
          </span>
        </nuxt-link>
      </li>
      <li >
        <nuxt-link to="/dashboard/customers">
          <i class="fa fa-th"></i> <span>Clientes</span>
          <span class="pull-right-container">
            <small class="label pull-right bg-green">new</small>
          </span>
        </nuxt-link>
      </li>
      <li >
        <nuxt-link to="/dashboard/providers">
          <i class="fa fa-th"></i> <span>Proveedores</span>
          <span class="pull-right-container">
            <small class="label pull-right bg-green">new</small>
          </span>
        </nuxt-link>
      </li>
      <li >
        <nuxt-link to="/dashboard/products">
          <i class="fa fa-th"></i> <span>Productos</span>
          <span class="pull-right-container">
            <small class="label pull-right bg-green">new</small>
          </span>
        </nuxt-link>
      </li>
      <li >
        <nuxt-link to="/dashboard/categories">
          <i class="fa fa-th"></i> <span>Categorias</span>
          <span class="pull-right-container">
            <small class="label pull-right bg-green">new</small>
          </span>
        </nuxt-link>
      </li>

    </ul>
  </section>
  <!-- /.sidebar -->
</aside>
</template>

<script>
export default {
    data(){
        return{
            name: 'Alejandro Cayssials'
        }
    }
}
</script>