<script>
    // import { onMount, onDestroy } from 'svelte';
    import {fade, scale} from 'svelte/transition'
    import FeedbackItem from "./FeedbackItem.svelte";
    import {FeedbackStore} from '../stores'

//     let feedback = []
//    const unsubscribe =  FeedbackStore.subscribe((data) => feedback = data)

//     onMount(() =>{

//     })

//     onDestroy(() => {
//         unsubscribe()
//     })
</script>

{#each $FeedbackStore as fb (fb.id) }
    <div in:scale out:fade>
        <FeedbackItem item={fb}/>
    </div>
{/each}