# work-report
## 关于svg颜色无法生效
原因：该颜色绑定其它svg id；
解决：保证id唯一；

# 移动端复制
    console.log('handleCopy');
    // 复制链接
    function copyLink(shareLink: string) {
      const input = document.createElement('input');
      input.setAttribute('readonly', 'readonly');
      input.setAttribute('value', shareLink);
      document.body.appendChild(input);
      input.focus();
      input.select();
      input.setSelectionRange(0, 9999);
      if (document.execCommand('copy')) {
        document.execCommand('copy');
        Toast({
          content: '复制成功',
          type: 'success',
          during: 1500
        });
      }
      document.body.removeChild(input);
      // 复制成功
    }
