<template>
  <div class="hello" id="html-print">

    <p class="amiri">السلام عليكم </p>
    <p class="amiri">كيف حالكم </p>
      <table class="table mb-0 table-bordered amiri">
          <thead class="card-header">
          <tr>
              <td class="col-3 amiri"><strong>Nature of goods or
                  services
                  تفاصیل السلع أو الخدمات</strong></td>
              <td class="col-2 text-center amiri"><strong>Unit price</strong><br><strong>سعر الوحدة</strong></td>
              <td class="col-1 text-center amiri"><strong>Quantity</strong><br><strong>الكمية</strong></td>
              <td class="col-3 text-end amiri"><strong>Item Subtotal (Including VAT)</strong><br><strong>المجموع (شامل ضریبة القیمة المضافة)</strong></td>
          </tr>
          </thead>
          <tbody>
          <tr>
              <td class="col-3 amiri">باقة رصيد تقارير - 200 تقرير تفصيلي</td>
              <td class="col-2 text-center amiri">6,000.00 SAR</td>
              <td class="col-1 text-center amiri">1</td>
              <td class="col-3 text-end amiri">6,900.00 SAR</td>
          </tr>
          </tbody>
          <tfoot class="card-footer amiri">
          <tr>
              <td colspan="3" class="text-end">
                  <sapn>الإجمالي الخاضع للضریبة (غیر شامل ضریبة القیمة
                      المضافة):</sapn> <br> <sapn>Total Taxable Amount (Excluding VAT)</sapn></td>
              <td class="text-end">6,000.00 SAR</td>
          </tr>
          <tr>
              <td colspan="3" class="text-end"><sapn>مجموع ضریبة القیمة المضافة:</sapn><br><sapn>Total VAT</sapn></td>
              <td class="text-end">900.00 SAR</td>
          </tr>
          <tr>
              <td colspan="3" class="text-end border-bottom-0"><sapn>إجمالي المبلغ المستحق:</sapn><br><sapn>Total Amount Due</sapn></td>
              <td class="text-end border-bottom-0">6,900.00 SAR</td>
          </tr>
          </tfoot>
      </table>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    msg: String
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.amiri {
    font-family: "Amiri";
}
</style>
