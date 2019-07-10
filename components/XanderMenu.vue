<template>
   <ul class="nav navbar-nav" id="menu">
    <li class="dropdown" id="menu-sales">
        <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true"
            aria-expanded="false">
            Ventas
            <span class="caret"></span>
        </a>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenu1">
            <li><nuxt-link to="/dashboard/sales.index">Comprobantes de venta...</nuxt-link></li>
            <li><nuxt-link to="/dashboard/sales.create">Nueva venta</nuxt-link></li>
            <li><nuxt-link to="#">Presupuestos</nuxt-link></li>
            <li><nuxt-link to="#">Pedidos</nuxt-link></li>
            <li role="separator" class="divider"></li>
            <li><nuxt-link to="#">Estadisticas</nuxt-link></li>
        </ul>
    </li>
    <li class="dropdown" id="menu-purchases">
        <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true"
            aria-expanded="false">
            Compras
            <span class="caret"></span>
        </a>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenu1">

            <li><nuxt-link to="/dashboard/tickets.index">Ver listado</nuxt-link></li>
            <li><nuxt-link to="/dashboard/orders.create">Nuevo...</nuxt-link></li>
            <li><nuxt-link to="/dashboard/orders.index">Ordenes de compra...</nuxt-link></li>
            <li><nuxt-link to="/dashboard/orders.create">Nueva orden de compra</nuxt-link></li>
            <li role="separator" class="divider"></li>
            <li><nuxt-link to="#">Estadisticas</nuxt-link></li>
        </ul>
    </li>
    <li class="dropdown" id="menu-config">
        <a id="drop2" href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true"
            aria-expanded="false">
            <i class="fa fa-gear"></i>
            <span class="caret"></span>
        </a>
        <ul class="dropdown-menu" aria-labelledby="dropdownMenu1">
            <li><nuxt-link to="/dashboard/shops.index">Sucursales</nuxt-link></li>
            <li><nuxt-link to="/dashboard/cash.index">Cajeros</nuxt-link></li>
            <li><nuxt-link to="/dashboard/trademarks.index">Marcas</nuxt-link></li>
            <li><nuxt-link to="/dashboard/categories.index">Categorias</nuxt-link></li>
            <li class="disable"><nuxt-link to="#">Roles</nuxt-link></li>
            <li role="separator" class="divider"></li>
            <li><nuxt-link to="/dashboard/admin.settings">Opciones...</nuxt-link></li>
        </ul>
    </li>
</ul>
 
</template>