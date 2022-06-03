<template>
    <v-container>
        <div
        class="d-flex justify-center mb-6 mt-7"
        >
            <v-spacer class="order-1 pa-2"></v-spacer>

            <div class="order-2 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-3 pa-2"></v-spacer>

            <div class="order-4 pa-2">
               <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-5 pa-2"></v-spacer>

            <div class="order-6 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>
            <v-spacer class="order-7 pa-2"></v-spacer>
        </div>
        <div
        class="d-flex justify-center mb-6"
        >
            <v-spacer class="order-1 pa-2"></v-spacer>

            <div class="order-2 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-3 pa-2"></v-spacer>

            <div class="order-4 pa-2">
               <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-5 pa-2"></v-spacer>

            <div class="order-6 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width="411px"
                    height="100px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>
            <v-spacer class="order-7 pa-2"></v-spacer>
        </div>
        <div
        class="d-flex justify-center mb-6"
        >
            <v-spacer class="order-1 pa-2"></v-spacer>

            <div class="order-2 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width= "629px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-3 pa-2"></v-spacer>

            <div class="order-4 pa-2">
               <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width= "629px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-5 pa-2"></v-spacer>
        </div>
        <div
        class="d-flex justify-center mb-6"
        >
            <v-spacer class="order-1 pa-2"></v-spacer>

            <div class="order-2 pa-2">
                <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width= "629px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-3 pa-2"></v-spacer>

            <div class="order-4 pa-2">
               <v-sheet
                    :color="`grey ${theme.isDark ? 'darken-2' : 'lighten-4'}`"
                    class="pa-3"
                >
                    <v-skeleton-loader
                    class="mx-auto"
                    width= "629px"
                    type="card"
                    ></v-skeleton-loader>
                </v-sheet>
            </div>

            <v-spacer class="order-5 pa-2"></v-spacer>
        </div>
    </v-container>
</template>

<script>
export default {
    setup() {
        
    },
    inject: {
      theme: {
        default: { isDark: false },
      },
    },
}
</script>

<style scoped>

</style>