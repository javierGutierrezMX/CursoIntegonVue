<template>
    <div>
        <ul>
            <li v-for="item in this.productos" v-bind:key="item.nombre">
            {{ item.nombre }} - {{ item.precio }} <input type="number" v-model="cantidades[item.id]"/>
            </li>
        </ul>
        <p>Total del carrito: {{total}}</p>
        <button  @click="calcularTotal">Agregar productos</button>
    </div>
</template>
<script>
export default{
    props: {
        
    },
    data(){
        return {
        total: 0,
        cantidades: [{"cantidadPulparindos": 0},  {"cantidadRocaletas": 0,},{"cantidadBocadines": 0}],
        productos: [{id: 0,nombre: "Pulparindo", precio: 5.50},{id: 1, nombre: "Rockaleta", precio: 8.00},{id: 2, nombre: "Bocadin", precio: 4.50}]
        }
    },
    methods:{
        calcularTotal: function() {
            this.total = 0;
            for (let index = 0; index < this.productos.length; index++) {
                let temptotal = this.cantidades[index] * this.productos[index].precio;
                console.log(temptotal);
                this.total += temptotal;
            }
        }
        }
    
}
</script>