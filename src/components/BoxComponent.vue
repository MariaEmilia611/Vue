<template>
    <div class="box">
        {{ Name }} - {{ age }}
        <span class="['status', status]"> - {{status}}</span>
    </div>
</template>
<script>
export default {
    name: 'BoxComponent',
    props: {
        name: {
            type: String,
            default: 'N/A'
        },
        age: {
            type: Number,
            required: true
        },
        status: {
            type: String,
            validator: value => ['active', 'inactive', 'pending'].includes(value),
            default: 'active'
        }
    }
}    
</script>

<style>
.active {
    background-color: green;
}

.inactive {
    background-color: red;
}

.pending {
    background-color: orange;
}

.box {
    width: 30px;
    height: 30px;
    background-color: yellow;
    justify-content: center;
    align-items: center;
    display: flex;
}
</style>