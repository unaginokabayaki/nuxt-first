<template>
    <div class="wrapper">
        <div class="container">
            <h1>Contact</h1>
            <p>お問い合わせ</p>
            <form action="" method="post">
                <label for="name">お名前</label>
                <input type="text" name="name" id="name" required>
                <label for="email">メール</label>
                <input type="text" name="email" id="email" required>
                <label for="content">ご要件</label>
                <textarea name="content" id="content" cols="30" rows="10"></textarea>
                <input type="submit" value="送信">
            </form>
        </div>
    </div>
</template>