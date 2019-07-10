<template>
    <div class="row">
        <div class="col-md-12">
            <div class="box">
                <div class="box-header with-border">
                    <h3 class="box-title">{{title}}</h3>
                </div>
                <!-- /.box-header -->

                <div class="box-body">
                    <slot></slot>
                </div>

            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: ['title'],
}
</script>
