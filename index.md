# 现实问题拆解工具

不提供建议，只呈现现实约束  
这是一个原型工具，不保证舒适体验

---

## 如何使用

请直接输入你当前最真实的问题。
不需要完整、不需要正确、不需要冷静。

---

## 本工具不会做什么

- 不给建议
- 不替你做判断
- 不提供情绪价值
- 不基于幻想或不存在的条件回应

---

## 你将看到什么

- 被忽略的现实条件
- 当前环境的客观约束
- 最可能发生的失败路径
- 阻碍性问题（而非答案）

---

## 重要说明

本工具不会提供结论或解决方案。
任何决策后果由使用者自行承担。
<!DOCTYPE html>
<html lang="zh">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>现实问题拆解工具</title>
</head>
<body>
    <h1>现实问题拆解工具</h1>
    <p>请输入你当前的真实问题，我们将通过现实约束来为你提供指导。</p>
    
    <form action="#" method="post">
        <label for="user-question">你的问题：</label>
        <textarea id="user-question" name="question" rows="4" cols="50"></textarea><br><br>

        <input type="submit" value="提交">
    </form>

    <div id="response-container">
        <h3>回复：</h3>
        <p>请提交你的问题后查看这里的反馈。</p>
    </div>

    <script>
        // 简单的表单处理脚本
        const form = document.querySelector('form');
        const responseContainer = document.getElementById('response-container');

        form.addEventListener('submit', function(event) {
            event.preventDefault(); // 防止页面刷新

            const question = document.getElementById('user-question').value;
            if (question) {
                responseContainer.innerHTML = `
                    <h3>回复：</h3>
                    <p>你提交的问题是：<b>${question}</b></p>
                    <p>根据我们的分析，当前问题的现实约束和风险是...</p>
                `;
            } else {
                responseContainer.innerHTML = '<p>请输入有效问题。</p>';
            }
        });
    </script>
</body>
</html>
