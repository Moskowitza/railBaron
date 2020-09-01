<script>
  const steps = {
    1: "Get Destination",
    2: "Get City",
    3: "Roll",
  };
  let step = steps[1];

  let roll = null;
  let oddEven = '';
  let territory= ''
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
  function getDestination() {
    roll = Math.floor(Math.random() * (13 - 2) + 2);
    oddEven = Math.round((Math.random())) ? 'odd' : 'even' 

  }
</script>

<style>
  div {
    background-color: blueviolet;
  }
</style>

<div>

  <h4>roll: {roll}</h4>
  <h4>Even/Odd: {oddEven}</h4>

 <h3>Territory {territory}</h3>

  <div>{step[1]}</div>
  
  <button on:click={() => getDestination()}>Get Destination</button>
</div>
