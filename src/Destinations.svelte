<script>
  let roll = null;
  let isOdd = false;
  const destinationTable = [
    { roll: 2, odd: "PLAINS", even: "SOUTHWEST" },
    { roll: 3, odd: "SOUTHEAST", even: "SOUTH CENTRAL" },
    { roll: 4, odd: "SOUTHEAST", even: "SOUTH CENTRAL" },
    { roll: 5, odd: "SOUTHEAST", even: "SOUTH CENTRAL" },
    { roll: 6, odd: "NORTH", even: "CENTRAL	SOUTHWEST" },
    { roll: 7, odd: "NORTH", even: "CENTRAL	SOUTHWEST" },
    { roll: 8, odd: "NORTHEAST", even: "PLAINS" },
    { roll: 9, odd: "NORTHEAST", even: "NORTHWEST" },
    { roll: 10, odd: "NORTHEAST", even: "NORTHWEST" },
    { roll: 11, odd: "NORTHEAST", even: "PLAINS" },
    { roll: 12, odd: "NORTHEAST", even: "NORTHWEST" },
  ];
  function getRandomArbitrary(min, max) {
    roll = Math.floor(Math.random() * (max - min) + min);
  }
</script>

<style>
  div {
    background-color: blueviolet;
  }
</style>


<div>
  {#if roll}
    <h4>{roll}</h4>
  {/if}

  <button on:click={() => getRandomArbitrary(2, 13)}>Roll</button>
</div>
