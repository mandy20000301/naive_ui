<template>
    <div class="container border grid grid-cols-4 gap-x-10">
        <n-ellipsis :line-clamp="4">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Architecto minima voluptatibus tenetur nam sapiente
            exercitationem molestiae, odit impedit omnis! Maiores error mollitia porro fugiat ducimus enim libero ipsam est
            debitis?
        </n-ellipsis>
        <n-ellipsis :line-clamp="4">
            Lorem ipsum dolor sit, amet consectetur adipisicing elit. Architecto minima voluptatibus tenetur nam sapiente
            exercitationem molestiae, odit impedit omnis! Maiores error mollitia porro fugiat ducimus enim libero ipsam est
            debitis?
            <template #tooltip>
                <div class="w-[200px]">
                    Lorem ipsum dolor sit, amet consectetur adipisicing elit. Architecto minima voluptatibus tenetur nam
                    sapiente
                    exercitationem molestiae, odit impedit omnis! Maiores error mollitia porro fugiat ducimus enim libero
                    ipsam est
                    debitis?
                </div>
            </template>
        </n-ellipsis>
    </div>
</template>
<script>

</script>