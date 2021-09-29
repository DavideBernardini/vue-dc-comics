<template>
    <main>
        <div class="in_progress">
            <div class="container">
                <h2>__Content goes here__</h2>
            </div>
        </div>
        <UsefullLinks/>
    </main>
</template>

<script>
import UsefullLinks from '@/components/UsefullLinks';

export default {
    name: 'Main',
    components: {
        UsefullLinks
    }
}
</script>

<style scoped lang="scss">
@import "@/assets/style/variables.scss";

.in_progress {
    height: 130px;
    background-color: #1c1c1c;
    color: #fff;
    line-height: 130px;
}
</style>