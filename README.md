
https://www.xbox.com/en-us/play/games/fortnite/bt5p2x999vh2

https://www.google.com/

data:text/html;charset=utf-8,%3Cbutton%20id%3D%22myBookmarklet%22%3ERun%20Bookmarklet%3C%2Fbutton%3E%0A%3Cscript%3E%0A%20%20document.getElementById('myBookmarklet').addEventListener('click'%2C%20function()%20%7B%0Avar%20sidebar%20%3D%20document.createElement('div')%3B%0Asidebar.style.position%20%3D%20'fixed'%3B%0Asidebar.style.top%20%3D%20'0'%3B%0Asidebar.style.right%20%3D%20'0'%3B%0Asidebar.style.width%20%3D%20'300px'%3B%0Asidebar.style.height%20%3D%20'100%25'%3B%0Asidebar.style.backgroundColor%20%3D%20'%23f4f4f4'%3B%0Asidebar.style.borderLeft%20%3D%20'2px%20solid%20%23ccc'%3B%0Asidebar.style.zIndex%20%3D%20'9999'%3B%0Asidebar.style.overflowY%20%3D%20'auto'%3B%0Asidebar.style.padding%20%3D%20'10px'%3B%0Asidebar.style.fontFamily%20%3D%20'Arial%2C%20sans-serif'%3B%0A%0Avar%20title%20%3D%20document.createElement('h2')%3B%0Atitle.textContent%20%3D%20'Saved%20Tabs'%3B%0Atitle.style.margin%20%3D%20'0'%3B%0Atitle.style.padding%20%3D%20'10px%200'%3B%0Asidebar.appendChild(title)%3B%0A%0Avar%20tabList%20%3D%20document.createElement('ul')%3B%0Asidebar.appendChild(tabList)%3B%0A%0Avar%20savedTabs%20%3D%20JSON.parse(localStorage.getItem('savedTabs'))%20%7C%7C%20%5B%5D%3B%0AsavedTabs.forEach(function(tab)%20%7B%0A%20%20%20%20addTab(tab)%3B%0A%7D)%3B%0A%0Afunction%20addTab(tab)%20%7B%0A%20%20%20%20var%20li%20%3D%20document.createElement('li')%3B%0A%20%20%20%20var%20a%20%3D%20document.createElement('a')%3B%0A%20%20%20%20a.href%20%3D%20tab.url%3B%0A%20%20%20%20a.textContent%20%3D%20tab.title%3B%0A%20%20%20%20a.style.color%20%3D%20'%23000'%3B%0A%20%20%20%20a.style.textDecoration%20%3D%20'none'%3B%0A%20%20%20%20li.appendChild(a)%3B%0A%20%20%20%20tabList.appendChild(li)%3B%0A%7D%0A%0Avar%20currentTab%20%3D%20%7B%0A%20%20%20%20title%3A%20document.title%2C%0A%20%20%20%20url%3A%20window.location.href%0A%7D%3B%0AsavedTabs.push(currentTab)%3B%0AaddTab(currentTab)%3B%0A%0AlocalStorage.setItem('savedTabs'%2C%20JSON.stringify(savedTabs))%3B%0A%0Avar%20closeBtn%20%3D%20document.createElement('button')%3B%0AcloseBtn.textContent%20%3D%20'Close'%3B%0AcloseBtn.style.marginTop%20%3D%20'20px'%3B%0AcloseBtn.onclick%20%3D%20function()%20%7B%0A%20%20%20%20document.body.removeChild(sidebar)%3B%0A%7D%3B%0Asidebar.appendChild(closeBtn)%3B%0A%0Adocument.body.appendChild(sidebar)%3B%0A%20%20%20%20alert('Hello%20from%20the%20bookmarklet!')%3B%20%0A%20%20%7D)%3B%0A%3C%2Fscript%3E%0A
