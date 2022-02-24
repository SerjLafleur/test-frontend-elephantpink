<template>
  <div>
    <transition name="fade">
      <div class="modal-overlay"></div>
    </transition>

    <transition name="fade">
      <div class="modal">
        <button class="button-close-modal">Close</button>
        <h3>Contact</h3>
        <p>
          Sed ut prerspiciates unde omnis iste natus error sit voluptam
          accusantium doloremque laudantium.
        </p>
        <form>
          <div>
            <input
              id="name"
              type="text"
              placeholder="Nombre"
              v-model="name"
              required
            />
          </div>
          <div>
            <input
              id="email"
              type="email"
              placeholder="Email"
              v-model="email"
              required
            />
          </div>
          <div>
            <textarea
              id="firstSon"
              placeholder="Your message here"
              v-model="firstSon"
              required
            ></textarea>
            <!-- <p class="error-modal">Unexpected server error ...</p> -->
          </div>

          <button
            class="submit-modal"
            :class="[name ? activeClass : '']"
            type="submit"
          >
            Send
          </button>
        </form>
      </div>
    </transition>
  </div>
</template>

<script>
export default {
  data() {
    return {
      showModal: false,
    };
  },
};
</script>
    
<style lang="scss" scoped>
.modal-overlay {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  z-index: 100;
  background: rgba(0, 0, 0, 0.6);
  overflow: hidden;
  height: 100%;
}
.modal {
  position: fixed;
  z-index: 101;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  background: #fff;
  padding: 20px;
}
form {
  min-width: 300px;
  padding: 10px 40px;
  input,
  textarea {
    border: 1px solid #ccc;
    color: #333;
    width: calc(100% - 30px);
  }
  input:focus,
  textarea:focus {
    border: 1px solid #c0984f;
    outline: none !important;
  }
  input:focus::placeholder,
  textarea:focus::placeholder {
    color: #000;
    font-weight: 500;
  }
  input,
  textarea,
  button {
    padding: 8px 15px;
    font-family: "Poppins", sans-serif;
    font-weight: 400;
  }
  textarea {
    height: 200px;
  }
  div {
    margin: 20px 0;
  }
}
.submit-modal {
  color: #000;
  border: none;
  width: 150px;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.08em;
  background: #c0984f;
  display: block;
  position: absolute;
  margin: 50px auto 0 auto;
  left: 150px;
  cursor: pointer;

  transition: 0.25s all ease;
  &:hover {
    transform: translateY(2px);
    background-color: rgb(191, 163, 111);
  }
}
.modal h3 {
  font-family: "Didot", sans-serif;
  text-transform: uppercase;
  text-align: center;
  font-size: 25px;
}
.modal p {
  width: 400px;
  text-align: center;
  font-family: "Poppins", sans-serif;
  font-size: 11px;
  color: #bbb;
}
.button-close-modal {
  border: none;
  background: transparent;
  position: absolute;
  margin-top: -50px;
  width: 0;
  font-weight: 200;
  font-size: 12px;
  letter-spacing: 1px;
  color: #fff;
}
</style>