<template>
   <div>
    <svg height="250" width="250" class="grafik">
            <!-- sehpa -->
            <line x1="50" y1="20" x2="130" y2="20"/>
            <line x1="130" y1="20" x2="130" y2="50"/>
            <line x1="50" y1="20" x2="50" y2="250"/>
            <line x1="10" y1="250" x2="90" y2="250"/>

            <!-- kafa -->
            <circle cx="130" cy="70" r="20" class="item"/>

            <!-- gövde -->
             <line x1="130" y1="90" x2="130" y2="170" class="item"/>

             <!-- kollar -->
            <line x1="130" y1="120" x2="100" y2="100"  class="item"/>
            <line x1="130" y1="120" x2="160" y2="100" class="item"/>

            <!-- bacaklar -->
            <line x1="130" y1="170" x2="100" y2="190" class="item"/>
            <line x1="130" y1="170" x2="160" y2="190" class="item"/>
        </svg>

   </div>
</template>


<script>
export default {
  name: 'Sekil'
}
</script>

<style>
.grafik {
  fill: transparent;
  stroke: #fff;
  stroke-width: 4px;
}

</style>