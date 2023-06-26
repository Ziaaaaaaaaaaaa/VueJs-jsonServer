<template>
    <div id="show">

    </div>
</template>

<script>
async function info(){
    let data = await fetch('https://ziaaaaaaaaaaaa.github.io/mehJsonServer/people.json')
    let test = await data.json()
    newJson = test.students

    console.log(newJson);

    let display = document.querySelector('#show')

    newJson.forEach(item =>{
        display.innerHTML +=`
            <p>${item.id}</p>
            <p>${item.first_name}</p>
            <p>${item.last_name}</p>
            <p>${item.email}</p>
        `
    })
}

info()
</script>

<style scoped>

</style>