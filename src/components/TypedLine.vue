<template>
    <div>
        {{ text_shown }} 
    </div>
</template>

<script>
    export default {
        name: 'TypedLine',
        props:{
            text: {
                type: String,
                required: true
            }
        },
        data(){
            return {
                min_typing_delay: 80,
                max_typing_delay: 200,

                text_shown: ''
            }
        },
        methods: {
            startTypingText(){
                let text = this.text;
                let text_shown = '';

                this.typeText(text, text_shown);
            },
            typeText(text, text_shown){
                if (text.length >= text_shown.length);
                    text_shown += text.charAt(text_shown.length);
                    this.text_shown = text_shown;
                    setTimeout(() => {
                        this.typeText(text, text_shown)
                    }, Math.floor(Math.random() * (this.max_typing_delay - this.min_typing_delay)) + this.min_typing_delay + 1);
            }
        },
        mounted(){
            this.startTypingText();
        }
    }
</script>