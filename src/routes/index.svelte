<script>
import {onMount} from 'svelte'
import RubiksFace from '$lib/RubiksFace.svelte'
const cubes = [["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"],
["w","y","g","o","b","r"]]

var str = ''

function findCube(cube){
	let rjekfo = cube[(Math.floor(Math.random()*cube.length))]
	str = str + rjekfo
	return rjekfo
}
</script>

{#each cubes as cube}
		<RubiksCube color={findCube(cube)}>
{/each}

{str}
