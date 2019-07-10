<template>
    <div>
        <table :id="datatable" class="table table-bordered table-striped">
            <thead>
                <tr role="row">                   
                    <th v-for="(item, index) in columns" :key="index" class="sorting_asc" tabindex="0" :aria-controls="datatable" rowspan="1" colspan="1"
                        aria-sort="ascending">
                        {{item}}
                    </th>
                </tr>    
            </thead>
        </table>
    </div>
</template>

<script>
export default {
    props: ['columns', 'datatable'],
}
</script>
