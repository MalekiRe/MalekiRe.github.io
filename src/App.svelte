<script>
    import {gun} from './initGun.js'
    let myVal = gun.get('message');

    let input = "null";
    myVal.on((data => input=data['message']))
</script>

<div class="app">
    <textarea bind:value={input} on:input={myVal.put({message: input})}></textarea>
</div>