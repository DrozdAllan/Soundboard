<template>
  <v-container>
    <v-row class="text-center">
      <v-col cols="12">
        Tableau des sons enregistrés
      </v-col>
    </v-row>
    <v-row class="text-center">
      <v-col>
        <v-simple-table>
          <thead>
          <tr>
            <th class="text-center">
              Sons enregistrés
            </th>
            <th class="text-center">
              Actions
            </th>
          </tr>
          </thead>
          <tbody>
          <tr>
            <td>
              Zinzin
            </td>
            <td>
              <v-btn>
                <v-icon @click="play()">mdi-play</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-pause</v-icon>
              </v-btn>
              <v-btn>
                <v-icon>mdi-stop</v-icon>
              </v-btn>
            </td>
          </tr>
          </tbody>
        </v-simple-table>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
	export default {
		name: 'Soundboard',

		data: () => ({
			// a
		}),
		methods: {
			play(audioName) {
				let audio = new Audio(require('@/assets/sounds/' + audioName));
				audio.play();
			}
		}
	}
</script>
