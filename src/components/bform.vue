<script setup lang="ts">
</script>

<template>
    <div class="tposition">
        <div class="rotate">
            <div class="scope">
                <span style="--i:1;"><img src="https://i.postimg.cc/BQcRL38F/pexels-photo-761963.jpg"
                        alt="not found"></span>
                <span style="--i:2;"><img src="https://i.postimg.cc/1RWVB11x/pexels-photo-941693.jpg"
                        alt="not found"></span>
                <span style="--i:3;"><img src="https://i.postimg.cc/CMfHRKfP/woman-2003647-960-720.jpg"
                        alt="not found"></span>
                <span style="--i:4;"><img src="https://i.postimg.cc/T1rDCpVT/beautiful-1274056-960-720.jpg"
                        alt="not found"></span>
                <span style="--i:5;"><img src="https://i.postimg.cc/SNf99YQr/woman-1807533-960-720.jpg"
                        alt="not found"></span>
                <span style="--i:6;"><img src="https://i.postimg.cc/2SHBcpZL/pexels-photo-4664520.jpg"
                        alt="not found"></span>
                <span style="--i:7;"><img
                        src="https://i.postimg.cc/CxBzNcjw/Opera-Snapshot-2020-07-03-162022-www-freepik-com.png"
                        alt="not found"></span>
                <span style="--i:8;"><img
                        src="https://i.postimg.cc/0QckxSpt/Opera-Snapshot-2020-07-03-161422-www-freepik-com.png"
                        alt="not found"></span>
            </div>
        </div>
        <div class="form">
            <div class="form-container">
                <h1>Send a Cute Message🤗🙄</h1>
                <form @submit.prevent="sendEmail">
                    <div>
                        <label for="name">😏--wht cn i cal u--</label>
                        <br><input type="text" id="name" placeholder="nick name..." v-model="form.name" required />
                    </div>
                    <div>
                        <label for="instagram">🙇--how we gossip--👻</label><br>
                        <input type="text" id="instagram" placeholder="insta or whatsapp..." v-model="form.instagram" required />
                    </div>
                    <div>
                        <label for="message">--a msg for mee--😲</label>
                        <br><textarea id="message"placeholder="waiting..." v-model="form.message" required></textarea>
                    </div>
                    <button type="submit">Send</button>
                </form>
                <div v-if="status" class="status">{{ status }}</div>
            </div>
        </div>
    </div>
</template>


<script>
import emailjs from 'emailjs-com';

export default {
    data() {
        return {
            form: {
                name: '',
                instagram: '',
                message: ''
            },
            status: ''
        };
    },
    methods: {
        sendEmail() {
            emailjs.send(
                'service_nlbtetl',
                'template_8g68nmm',
                this.form,
                'ukihWQAISq14-MJ2N'
            ).then((response) => {
                this.status = 'I will Catch You Soon🥰🥰💕💕!';
                this.form = {
                    name: '',
                    instagram: '',
                    message: ''
                };
            }).catch((error) => {
                this.status = 'Failed to send message. Please try again.';
            });
        }
    }
};
</script>


<style scoped>
.tposition {
    display: grid;
    grid-template-rows: auto;
    gap: 10%;
    text-align: left;
    padding: 10px;
}

.rotate {
    box-sizing: border-box;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 50vh;
    background: #dddfe0ca;
    background: -webkit-linear-gradient(to right, #ebf2f5b7, #eeeaead3, #e7edef5b);
    overflow: hidden;
    border-radius: 5%;
}

.scope {
    position: relative;
    width: 100px;
    height: 100px;
    transform-style: preserve-3d;
    animation: slid 30s linear infinite;
}

.scope span {
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    transform-origin: center;
    transform-style: preserve-3d;
    transform: rotateY(calc(var(--i) * 45deg)) translateZ(250px);
}

.scope span img {
    position: absolute;
    top: 0;
    left: 0;
    width: 150%;
    height: 150%;
    border-radius: 10px;
    object-fit: cover;
    transition: 2s;
}

.scope span:hover img {
    transform: translateY(-40px) scale(1.7);
}

@keyframes slid {
    0% {
        transform: perspective(1000px) rotateY(0deg);
    }

    100% {
        transform: perspective(1000px) rotateY(360deg);
    }
}

/* form */
.form-container {
    max-width: 600px;
    margin: auto;
    padding: 2rem;
    background: #ffe4e1a8;
    border-radius: 10px;
    box-shadow: 0 25px 25px rgba(227, 58, 201, 0.766);
}

h1 {
    text-align: center;
    color: #ff69b4;
}

form {
    display: flex;
    flex-direction: column;
}

label {
    margin-bottom: 0.5rem;
    color: #ff1493;
}

input,
textarea {
    padding: 0.5rem;
    margin-bottom: 1rem;
    border: 2px solid #ff69b4;
    border-radius: 5px;
}

button {
    padding: 0.5rem;
    background: #ff69b4;
    border: none;
    border-radius: 5px;
    color: white;
    cursor: pointer;
}

button:hover {
    background: #ff1493;
}

.status {
    text-align: center;
    margin-top: 1rem;
    color: #ff143f;
}


@media screen and (max-width:769px) {
.tposition{
    text-align: center;
    padding: 0 0 0 7%;
}
}

@media screen and (max-width:446px) {
.tposition{
    padding: 0 0 0 0;
}
}

</style>
