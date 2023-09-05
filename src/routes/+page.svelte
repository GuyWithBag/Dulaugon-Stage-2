<script lang="ts">
	import Card from "$lib/components/card.svelte"
    import portrait from "$lib/assets/images/portraits/portrait.jpg" 
    import Person from '$lib/classes/person'

    let personList: Person[] = [
        new Person(
            "Bluth, George", 
            "george.bluth@reques.in", 
            portrait
        ), 
        new Person(
            "Weaver, Janeth", 
            "janet.weaver@reques.in", 
            portrait
        ), 
        new Person(
            "Wong, Emma", 
            "emma.wong@reques.in", 
            portrait
        ), 
        new Person(
            "Holt, Eve", 
            "eve.holt@reques.in", 
            portrait
        ), 
        new Person(
            "Morris, Charles", 
            "charles.morris@reques.in", 
            portrait
        ), 
        new Person(
            "Ramos, Tracey", 
            "tracey.ramosh@reques.in", 
            portrait
        )
    ]

</script>

<div class="flex flex-col gap-5 items-center content-center justify-center p-10 lg:p-20">
    <div class="flex items-center content-center justify-center">
        <div class="grid grid-cols-2 lg:grid-cols-3 gap-5"> 
            {#each personList as person, index}
                <Card 
                    avatar="{person.avatar}"
                    id="{(index + 1).toString()}" 
                    name="{person.name}"
                    email="{person.email}"
                />
            {/each}
        </div>
    </div>
</div>



