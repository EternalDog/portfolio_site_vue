<template>
    <div id="self_div">

        <h1>About me</h1>


        <div id="text">

            <p>
                I am a Polish Programmer and Web Developer who recently came from Ireland to England.
                Earlier this year I have finished a degree (BSc Web Development) in the Cork Institute of Technology. 
                Last year I have also worked as an intern software engineer at McAfee, which I found to be a pretty positive experience.
                I am pretty passionate about programming and IT in general, and my current goal in life is to continue expanding my existing skills.
            </p>

            <h3>Some of my interests:</h3>
            <ul>
                <li>I am something of a serious history enthusiast, I also take part in organised historical reenactment as part of the group “Historia Normannis”. </li>
                <li>I took part in various charity events for animal rights, such as taking part in a few protests against dog cruelty in Cork. </li>
                <li>I volunteered for the 2019 CIT Open Data Hackathon, a 12 hour programming event. </li>
                <li>I am pretty passionate about dogs. Cats are alright. </li>
                <li>I occasionally engage in photography, and once every 50 or so photos I actually manage to take a good one. (The photos on this site are mine). </li>
                <li>I enjoy cycling. I also do some more uncommon sports such as hiking or skiing. </li>
                <li>I am an avid reader of fiction, fantasy and history books. My favourite author would probably Terry Pratchett. </li>
                <li>Model Building is another hobby of mine, I like it because it’s something that lets me use my more artistic and creative side. </li>
                <li>Airsoft, a few years ago I took part in a big charity event called “make your mark on cancer” in Ireland that raised almost 2 thousand euro. </li>
            </ul>
        </div>
 
    </div>
</template>
<script>
export default {
    name: "self",

    
}
</script>
<style lang="scss" scoped>
    #self_div {
        border-style: solid;
    }

    ul {
        list-style-type: square;
        text-align: left;
    }

    #text {
        margin: 0px 15vw 0px 15vw;
        color: black;
        background-color: rgba(255, 255, 255, 0.3);
        padding: 15px;
        border-radius: 5px;
    }
</style>