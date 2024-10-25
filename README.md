
https://www.xbox.com/en-us/play/games/fortnite/bt5p2x999vh2

https://www.google.com/



<button onclick="yourBookmarkletFunction()">Run Bookmarklet</button>

<script>
function yourBookmarkletFunction() {
  // javascript:(function() {
    // Create the sidebar container
    var sidebar = document.createElement('div');
    sidebar.style.position = 'fixed';
    sidebar.style.top = '0';
    sidebar.style.right = '0';
    sidebar.style.width = '300px';
    sidebar.style.height = '100%';
    sidebar.style.backgroundColor = '#f4f4f4';
    sidebar.style.borderLeft = '2px solid #ccc';
    sidebar.style.zIndex = '9999';
    sidebar.style.overflowY = 'auto';
    sidebar.style.padding = '10px';
    sidebar.style.fontFamily = 'Arial, sans-serif';

    // Create the title
    var title = document.createElement('h2');
    title.textContent = 'Saved Tabs';
    title.style.margin = '0';
    title.style.padding = '10px 0';
    sidebar.appendChild(title);

    // Create the list of tabs
    var tabList = document.createElement('ul');
    sidebar.appendChild(tabList);

    // Load saved tabs from localStorage
    var savedTabs = JSON.parse(localStorage.getItem('savedTabs')) || [];

    savedTabs.forEach(function(tab) {
        addTab(tab);
    });

    // Function to add a tab to the sidebar
    function addTab(tab) {
        var li = document.createElement('li');
        var a = document.createElement('a');
        a.href = tab.url;
        a.textContent = tab.title;
        a.style.color = '#000';
        a.style.textDecoration = 'none';
        li.appendChild(a);
        tabList.appendChild(li);
    }

    // Add the current tab to the list
    var currentTab = {
        title: document.title,
        url: window.location.href
    };
    savedTabs.push(currentTab);
    addTab(currentTab);

    // Save the updated tabs to localStorage
    localStorage.setItem('savedTabs', JSON.stringify(savedTabs));

    // Create a button to close the sidebar
    var closeBtn = document.createElement('button');
    closeBtn.textContent = 'Close';
    closeBtn.style.marginTop = '20px';
    closeBtn.onclick = function() {
        document.body.removeChild(sidebar);
    };
    sidebar.appendChild(closeBtn);

    // Append the sidebar to the body
    document.body.appendChild(sidebar);
})();
}
</script>

