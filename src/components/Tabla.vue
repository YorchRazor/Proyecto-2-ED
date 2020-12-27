<template>
<div>
    {{ booleanToChar(p) }} |
    {{ booleanToChar(q) }} |
    {{ booleanToChar(cadenaToBoolean(cadena, p, q)) }}
  </div>

</template>

<script>
export default {
  props: ["p", "q", "cadena"],
  methods: {
    cadenaToBoolean(cadena, p, q) {
      return eval(
        cadena
          .replace(/p/gi, p)
          .replace(/q/gi, q)
          .replace(/<->/gi, "===")
          .replace(/->/gi, "<=")
          .replace(/\^/gi, "&&")
          .replace(/v/gi, "||")
          .replace(/\¬/gi, "!")
      );
    },
    booleanToChar(operador) {
      return operador === true ? "V" : "F";
    }
  }
};
</script>

