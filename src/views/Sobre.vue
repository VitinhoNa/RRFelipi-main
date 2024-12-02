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
      </div>
          <!-- Mapa da Localização -->
    <div class="location">
      <h2>Localização</h2>
      <div class="map-container">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d7318.747876416907!2d-46.721299!3d-23.483037!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x94cef9132a6c0a83%3A0xeb98f37107c61bbd!2sAv.%20Miguel%20de%20Castro%2C%20106%20-%20Vila%20Pereira%20Barreto%2C%20S%C3%A3o%20Paulo%20-%20SP%2C%2002950-000%2C%20Brasil!5e0!3m2!1spt-PT!2sus!4v1733171341758!5m2!1spt-PT!2sus"
          width="700"
          height="400"
          style="border:0; border-radius: 10px;"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
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
    justify-content: flex-start; /* Ajustado para que o conteúdo fique no topo */
    align-items: center; /* Alinhamento central horizontal */
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
  
  .sobre h1, .sobre h2 {
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
  