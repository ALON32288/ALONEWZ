// טוען פוסטים מקובץ JSON שנוצר ע"י ה-CMS
fetch('/posts.json')
  .then(res => res.json())
  .then(posts => {
    const container = document.getElementById('posts');
    posts.forEach(post => {
      const div = document.createElement('div');
      div.className = 'post';
      div.innerHTML = `<h2>${post.title}</h2><p>${post.body}</p>`;
      container.appendChild(div);
    });
  });
