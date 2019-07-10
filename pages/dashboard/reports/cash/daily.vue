<template>
  <div>

    <!-- Content Header (Page header) -->
    <section class="content-header">
      <h1>Movimientos del día</h1>
      <xander-breadcumb section="Reportes" />
    </section>

    <!-- Main content -->
    <section class="content">
      <div class="card">
        <div class="card-block m-t-35" id="user_body">
          <div class="table-toolbar">
            <div class="btn-group">
              <xander-button url="#" icon="fa fa-print">Imprimir</xander-button>
              <xander-button url="#" icon="fa fa-envelope">Enviar por E-Mail</xander-button>
            </div>
          </div>
        </div>

        <xander-box title="Caja: Movimientos del dia">
          <xander-datatables-header :columns="['Fecha', 'Concepto','Entrada','Salida','Acciones']"
            datatable="reports" />
        </xander-box>

      </div>

    </section>
    <!-- /.content -->


  </div>
</template>

<script>

  if (process.BROWSER_BUILD) {
    const $ = require('jquery')
    $(function() {
        console.log('document ready!');
        // do whatever you want with html and jquery
    })
  
  function loadData() {
    $.ajaxSetup({
      headers: {
        'X-CSRF-TOKEN': $('meta[name="csrf-token"]').attr('content')
      }
    });

    $('#reports').DataTable({
      processing: true,
      serverSide: true,
      ajax: {
        "url": "{{ url(" / api / dashboard / datatables / reports_cash_daily / ") }}",
        "dataType": "json",
        "type": "post",
        "data": {
          _token: "{{csrf_token()}}"
        }
      },
      columns: [{
          data: 'created_at',
          name: 'created_at'
        },
        {
          data: 'concept',
          name: 'concept'
        },
        {
          data: 'in',
          name: 'in'
        },
        {
          data: 'out',
          name: 'out'
        },
        {
          data: 'options',
          name: 'options',
          orderable: false,
          searchable: false
        }
      ]
    });

  }

  $(document).ready(function () {
    loadData();
    $('.dataTables_filter input').addClass("form-control input-sm");

  });

}

import XanderBreadcumb from "~/components/XanderBreadcumb";
import XanderButton from "~/components/XanderButton";
import XanderBox from "~/components/XanderBox";
import XanderDatatablesHeader from "~/components/XanderDatatablesHeader";

export default {
 layout: 'admin',
 components: {
     XanderBreadcumb, XanderButton, XanderDatatablesHeader, XanderBox
 }   
}

</script>
