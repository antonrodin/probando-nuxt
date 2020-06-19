<template>
    <div>
        <h1>Todos los tiempos de Nürburgring</h1>
        <p>En esta tabla podrás encontrar los mejores records del circuito de Nürburgring, este circuito, apodado "El Infierno Verde", es esencial para las pruebas de los coches modernos. Sacar aquí unas décimas a un coche de la competencia no solo te hace más rápido, sino más rico ya que ser el mas rápido aquí, te convierte por ejemplo en la referencia para mucha gente que va a comprar ese coche. Por ello hay equipos de probadores de Jaguar o de Nissan cerca del circuito, así como muchos profesionales del sector automovilístico alrededor, sacando pruebas, haciendo fotos o simplemente divirtiendose. Se puede llamar la meca del automovilismo moderno y de todo amante de coches en general.</p>

        <hr>

        <h2>Tenemos en total {{ total }} tiempos en la BD</h2>
        <div v-for="record in records" :key="record.id">
            <p>{{ record.marca }} - {{ record.modelo }}</p>
        </div>

    </div>
</template>

<script>
export default {
    head() {
        return {
            title: "Todos los tiempos de Nürburgring",
            meta: [
                { hid: "description", name: "description", content: "En esta tabla podrás encontrar los mejores records del circuito de Nürburgring, este circuito, apodado" }
            ]
        }
    },

    async asyncData({ $axios }) {
        let response = await $axios.$get("/records");
        
        return response;
    },

    // data() {
    //     return {
    //         records: [],
    //         total: 0
    //     }
    // },

    // created() {
    //     this.$axios.$get("http://localhost:3001/api/records").then(response => {
    //         this.records = response.records;
    //         this.total = response.total;
    //     });
    // }

}
</script>