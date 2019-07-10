<template>
    <div id="app" class="hold-transition skin-blue sidebar-mini">
        
    <div class="wrapper">

        <xander-header />

        <xander-sidebar />
        <!-- Content Wrapper. Contains page content -->
        <div class="content-wrapper">
            <nuxt />
        </div>
        <!-- /.content-wrapper -->

        <xander-footer />

        <!-- Add the sidebars background. This div must be placed
       immediately after the control sidebar -->
        <div class="control-sidebar-bg"></div>

    </div>
    </div>
    <!-- ./wrapper -->
</template>

<script>
import XanderHeader from '~/components/XanderHeader.vue'
import XanderSidebar from '~/components/XanderSidebar.vue'
import XanderFooter from '~/components/XanderFooter.vue'

export default {
    
    components: {
    XanderHeader,
    XanderSidebar,
    XanderFooter,
  }
    
}
</script>
