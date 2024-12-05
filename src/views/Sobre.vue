<template>
  <div class="main">
    <div class="sobre">
      <h1>A Empresa</h1>
      <p><strong>{{ empresa.nome }}</strong> {{ empresa.descricao1 }}</p>
      <p>{{ empresa.descricao2 }}</p>
      <p>{{ empresa.descricao3 }}</p>
      <h2>Nossos Serviços</h2>
      <ul>
        <li v-for="servico in empresa.servicos" :key="servico">{{ servico }}</li>
      </ul>
      <p><strong>{{ empresa.horario }}</strong></p>
      <a href="https://wa.me/SEUNUMERO" target="_blank" class="contact-button">
        <i class="fab fa-whatsapp icon"></i> Entre em Contato
      </a>
    </div>
    <!-- Mapa da Localização -->
    <div class="location">
      <h2>Localização</h2>
      <div class="map-container">
        <h2 class="map-title">Localização</h2>
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d7318.747876416907!2d-46.721299!3d-23.483037!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94cef9132a6c0a83%3A0xeb98f37107c61bbd!2sAv.%20Miguel%20de%20Castro%2C%20106%20-%20Vila%20Pereira%20Barreto%2C%20S%C3%A3o%20Paulo%20-%20SP%2C%2002950-000%2C%20Brasil!5e0!3m2!1spt-PT!2sus!4v1733171341758!5m2!1spt-PT!2sus"
          width="700" height="400" style="border:0; border-radius: 10px;" allowfullscreen="" loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"></iframe>
      </div>
    </div>
  </div>
</template>

<style>
.main {
  background: url('@/assets/ImagemSobreFundo.jpg') no-repeat center center fixed;
  background-size: cover;
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  justify-content: flex-start;
  align-items: center;
  padding: 20px;
}

.sobre {
  font-family: 'Arial', sans-serif;
  max-width: 800px;
  background-color: rgba(255, 255, 255, 0.9);
  padding: 30px;
  border-radius: 10px;
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.2);
  color: #333;
}

.sobre h1,
.sobre h2 {
  text-align: center;
  color: #cf2a2a;
  margin-bottom: 20px;
}

.sobre p {
  line-height: 1.8;
  margin-bottom: 20px;
}

.sobre ul {
  list-style-type: disc;
  padding-left: 20px;
  margin: 20px 0;
}

.sobre ul li {
  margin-bottom: 10px;
}

.sobre p:last-of-type {
  text-align: center;
  font-weight: bold;
  margin-top: 30px;
}

.location {
  font-family: 'Arial', sans-serif;
  font-size: 23px;
  font-weight: bold;
  color: #cf2a2a;
  text-align: center;
  margin-bottom: 20px;
}

.map-container {
  position: relative;
  width: 700px;
  max-width: 90%;
  text-align: center;
}

.map-title {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  font-family: 'Arial', sans-serif !important;
  font-size: 24px !important;
  font-weight: bold !important;
  color: #cf2a2a !important;
  z-index: 1;
  background: rgba(255, 255, 255, 0.8);
  padding: 5px 10px;
  border-radius: 5px;
  text-align: center;
}

.contact-button {
  display: flex;
  align-items: center;
  justify-content: center;
  margin: 10px auto;
  text-decoration: none;
  background-color: #25d366;
  color: white;
  font-size: 14px;
  font-weight: bold;
  padding: 6px 12px;
  border-radius: 10px;
  box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2);
  width: auto;
  height: auto;
  transition: transform 0.2s, box-shadow 0.2s;
  line-height: 1.2;
}

.contact-button:hover {
  transform: scale(1.05);
  box-shadow: 0 4px 10px rgba(0, 0, 0, 0.3);
}

.contact-button .icon {
  width: 10px;
  height: 10px;
  margin-right: 10px;
}
</style>

<script>
export default {
  data() {
    return {
      empresa: {
        nome: "RRFELIPI PROJETOS E ASSESSORIA IMOBILIÁRIA",
        descricao1:
          "iniciou suas atividades visando construir a sua história no mercado da construção civil e imobiliário de São Paulo, de forma sólida, confiável e duradoura.",
        descricao2:
          "Trata-se de Assessoria imobiliária atuante no mercado, com um histórico íntegro e de ótimas negociações. Ética profissional e transparência são imprescindíveis no mercado imobiliário.",
        descricao3:
          "A busca pela excelência é à maneira crescente neste mercado, sendo assim, a RRFELIPI PROJETOS E ASSESSORIA IMOBILIÁRIA oferece para os seus clientes um atendimento personalizado, o que resulta em segurança a todos os negócios realizados, satisfazendo os nossos clientes.",
        servicos: [
          "CND",
          "Desdobro de IPTU",
          "Averbação de Obra",
          "Certificado de Conclusão",
          "Aprovações de Plantas",
          "Alvará de Desdobro de Lote",
          "Certidões Junto à Prefeitura",
          "Regularização de Residência",
        ],
        horario: "Segunda a Sexta das 8 às 17:30",
      },
    };
  },
};
</script>