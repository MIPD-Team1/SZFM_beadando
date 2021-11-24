<template>
  <div class="bg">
    <div class="text">
      <h1>
        Legjobb Webshop Ever
      </h1>
      <h2>
        Ez a webshop nem csak egy a sok közül, nem, ez a valaha volt legjobb webshop.
      </h2>
      <h3>
        Nálunk forradalmi módon válogathat termékeink közül, melyeket hozzáértő szakembereink állítottak össze páratlan
        szakértelemmel.
        Természetesen a kiszemelt termékeket meg is rendelheti, sőt, ehhez még csak regisztrálnia sem kell oldalunkra.
        Azonban mindenkit ösztönzünk a regisztálásra, ugyanis ezáltal olyan soha nem látott szolgáltatások válnak
        elérhetővé, mint:
      </h3>
      <h4>
        - Kedvenc termékeinek elmentése, eltárolása, szerkesztése, megtekintése a Kedvencek oldal által.
      </h4>
      <h4>
        - Kedvenc termékeinek bármikori megrendelése, külön-külön, de akár egyben is.
      </h4>
      <h4>
        - Adatainak eltárolásával jelentősen gyorsabbá, hatékonyabbá tehetjük vásárlásra fordított idejét.
      </h4>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style scoped>

.bg {
  height: 600px;
  position: relative;
  padding: 30px;
  box-sizing: border-box;
  background-image: url('~assets/images/assad.jpg');
  background-position: center;
  background-size: cover;

}

.text {
  background-color: whitesmoke;
  border-radius: 10px;
  box-shadow: 3px 3px 3px black;
  box-sizing: border-box;
  border: 1px solid black;
}

h1, h2, h3 {
  text-align: center;
}

h3 {
  margin: 0.5in;

}

h4 {
  margin-left: 1in;
  text-align: left;
}

</style>
