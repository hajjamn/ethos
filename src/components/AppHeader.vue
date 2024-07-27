<script>

export default {
  components: {
  },
  data() {
    return {
    }
  },
  mounted() {
    document.addEventListener('DOMContentLoaded', () => {
      const squares = document.querySelectorAll('.square');

      setTimeout(() => {
        squares.forEach(square => {
          if (square.dataset.color === 'red') {
            square.classList.add('flipped');
          }
        });
      }, 1000); // Adjust the delay as necessary
    });
  }
}

</script>

<template>

  <header>
    <section id="logo-section" class="bg-dark">
      <div class="container py-5 text-center text-white">
        <div class="row justify-content-between align-items-center">
          <!-- LOGO -->
          <div class="col-auto">
            <div class="logo-container">
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="grey"></div>

              <div class="square" data-color="red"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>

              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="grey"></div>

              <div class="square" data-color="red"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>
              <div class="square" data-color="grey"></div>

              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="red"></div>
              <div class="square" data-color="grey"></div>

              <div class="square-letter">E</div>
              <div class="square-letter">T</div>
              <div class="square-letter">H</div>
              <div class="square-letter">O</div>
              <div class="square-letter">S</div>
            </div>
          </div>
          <div class="col-auto">
            <h1 class="">STUDIO LEGALE ASSOCIATO</h1>
          </div>
          <div class="col-auto">

            <div class="dropdown">
              <button class="btn btn-secondary dropdown-toggle" type="button" data-bs-toggle="dropdown"
                aria-expanded="false">
                <font-awesome-icon :icon="['fas', 'bars']" />
              </button>
              <ul class="dropdown-menu">
                <li><a class="dropdown-item" href="#">Chi siamo</a></li>
                <li><a class="dropdown-item" href="#">Il nostro lavoro</a></li>
                <li><a class="dropdown-item" href="#">Lo studio</a></li>
                <li><a class="dropdown-item" href="#">Dove lavoriamo</a></li>
                <li><a class="dropdown-item" href="#">Le persone</a></li>
                <li><a class="dropdown-item" href="#">Strumenti</a></li>
                <li><a class="dropdown-item" href="#">Mappe</a></li>
              </ul>
            </div>
          </div>
        </div>
      </div>
    </section>
  </header>

</template>

<style scoped>
#logo-section {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 0;
  background-color: #f0f0f0;
}

.logo-container {
  display: grid;
  grid-template-columns: repeat(5, 20px);
  grid-template-rows: repeat(6, 20px);
  gap: 2px;
}

.square {
  width: 20px;
  height: 20px;
  background-color: grey;
  transition: transform 0.6s, background-color 0.6s;
  transform-style: preserve-3d;
}

.square-letter {
  width: 20px;
  height: 20px;
}

.square.flipped {
  transform: rotateY(180deg);
}

.square[data-color="red"].flipped {
  background-color: red;
}
</style>