<template lang="pug">
section
  BannerPrincipal.mb-5


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 1. Presentación

    p Bienvenido apreciado aprendiz al programa de formación complementaria de acreditación en salud, el cual le permitirá implementar una herramienta de mejora continua y aplicar técnicas para los procesos de evaluación externa, el acceso gradual y continuo de las entidades que conforman el sector  e impactar en la calidad de vida de los usuarios del sistema general de seguridad social, además de los indicadores sociales del país, a través de contenidos que le permitan reconocer las normas asociadas al proceso de acreditación, aplicar estándares para realizar la autoevaluación e implementar planes de mejora, la formación está dirigida al talento humano en salud y personal administrativo del sector.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 2. Justificación del programa

    p El sistema único de acreditación en salud busca el mejoramiento gradual y continuo de las entidades que conforman el sector salud fortaleciendo la eficacia, eficiencia y resultados en salud, impactando positivamente en la calidad de vida de la población e indicadores sociales del país.
    br
    |Esta formación complementaria está dirigida al talento humano en salud y personal administrativo de este sector, donde sus decisiones en aspectos de calidad intervienen en los procesos propios institucionales y se interrelacionan en el marco de la acreditación en salud. Adicionalmente, se busca el desarrollo de herramientas de mejora continua que permitan aumentar la competitividad garantizando condiciones seguras en la atención en salud.


  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 3. Competencias desarrollar 

    p 
      b 230101266- 
      b-none Orientar personas según normativa de salud.

  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 4. Perfil de ingreso

    ul.lista-ul
        li 
          i.lista-ul__vineta
          | Talento humano en salud.
        li 
          i.lista-ul__vineta
          | Personal administrativo del sector salud.
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 5. Perfil de egreso
    p No aplica.
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.pb-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 6. Estrategia metodológica
    p Centrada en la construcción de autonomía para garantizar la calidad de la formación en el marco de la formación por competencias, el aprendizaje por proyectos y el uso de técnicas didácticas activas que estimulan el pensamiento para la resolución de problemas simulados y reales; soportadas en el utilización de las tecnologías de la información y la comunicación, integradas, en ambientes virtuales de aprendizaje, que en todo caso recrean el contexto productivo y vinculan al aprendiz con la realidad cotidiana y el desarrollo de las competencias. 
      br
      br
      |Igualmente, debe estimular de manera permanente la autocrítica y la reflexión del aprendiz sobre el quehacer y los resultados de aprendizaje que logra a través de la vinculación activa de las cuatro fuentes de información para la construcción de conocimiento:
    ul.lista-ul.mt-3
        li 
          i.lista-ul__vineta
          | El instructor – tutor.
        li 
          i.lista-ul__vineta
          | El entorno.
        li 
          i.lista-ul__vineta
          | Las TIC.
        li 
          i.lista-ul__vineta
          | El trabajo colaborativo.
    


  //- Créditos
  .container.tarjeta.tarjeta__template--azul-claro.px-3.py-4.px-sm-5.mb-5
    .titulo__template--a.mb-4
      span.h6 Créditos


    CreditosComp

  Footer
  

</template>
<script>
import { menuPrincipal } from '../config/global'
import BannerPrincipal from '../components/plantilla/BannerPrincipal'
import CreditosComp from '../components/plantilla/CreditosComp'
import Footer from '../components/plantilla/Footer'
export default {
  name: 'Inicio',
  components: {
    BannerPrincipal,
    CreditosComp,
    Footer,
  },
  data: () => ({
    menuPrincipalData: menuPrincipal,
  }),
  computed: {
    desarrolloContenidosData() {
      const allMenuData = [
        ...this.menuPrincipalData.menu,
        ...this.menuPrincipalData.subMenu,
      ]
      return allMenuData.filter(item => item.desarrolloContenidos)
    },
  },
}
</script>

<style lang="sass" scoped>
.resultados-aprendizaje
  &__item
    margin-bottom: 20px
    &:last-child
      margin-bottom: 0

.desarrollo-contenidos
  &__item
    display: flex
    align-items: center
    justify-content: space-between
    margin-bottom: 25px
    padding: 5px
    border-radius: $base-border-radius

    &__texto
      display: flex
      align-items: center

    &__icono
      display: block
      background-color: $color-sistema-g
      font-size: 20px
      font-weight: $base-black-font-weight
      text-align: center
      padding: 10px
      line-height: 1em
      width: 40px
      margin-right: 15px

    &:last-child
      margin-bottom: 0

    &:hover
      background-color: $color-sistema-g
      font-weight: $base-black-font-weight
      color: $color-sistema-a
</style>
