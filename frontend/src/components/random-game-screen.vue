/**
* Copyright (C) 2017 by Oxford 2017 Group Design Practical Team 9
*
* This file is part of GroupDesignBattleship.
*
* GroupDesignBattleship is free software: you can redistribute it
* and/or modify it under the terms of the GNU Affero General Public
* License as published by the Free Software Foundation, either
* version 3 of the License, or (at your option) any later version.
*
* GroupDesignBattleship is distributed in the hope that it will be
* useful, but WITHOUT ANY WARRANTY; without even the implied warranty
* of MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the GNU
* Affero General Public License for more details.
*
* You should have received a copy of the GNU Affero General Public
* License along with GroupDesignBattleship. If not, see
* <http://www.gnu.org/licenses/>.
*/

<template>
  <p>Waiting for an opponent...</p>
</template>

<script>
export default {
  name: 'random-game-screen',
  mounted() {
    this.$store.dispatch('waitForPlayer', {
      okCallback: () => {
        this.$emit('changeScreen', 'game')
      },
    })
  },
}
</script>

<style lang="scss">
</style>
