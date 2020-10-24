<template>
  <div id="app">
    <v-main>
      <Editor
        mode="preview"
        ref="editor"
        hint="Hint"
        :outline="false"
        :render-config="renderConfig"
        v-model="text"

        rows="12"
      />
      <router-view/>
    </v-main>
  </div>
</template>

<script>
import { Editor } from "vuetify-markdown-editor";
export default {
  name: 'App',

  components: {
    Editor
  },

  data: () => ({
    // for editor
    text: "",
    renderConfig: {
      // Mermaid config
      mermaid: {
        theme: "dark"
      }
    }  
  }),
  mounted(){
    this.$refs.editor.$props;
  },
};
</script>
