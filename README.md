# optimized-image-loading

This repo contains index.html file inside which it has javascript code in <Script> tag which can be used to optimize the image loading

 imageUrls.forEach(user => {
    const imageUrl = user.image;
    const img = new Image();
    img.src = imageUrl;
});

Whenever the user loads this page for first time this loop runs and caches the image element to browser
and on next load images are fetched from browser cache

to experience the differece we use following steps
- go to chrome developer tool for this page
- go to network and check the disable cache and set throttling to slow 3g and now reload page 2 3 times, page will each time load the image from source url and take more time to load
- now uncheck the disable cache and keep throttling to slow 3g and now reload, on first load page may take time and cache the image to browser and on next load loading time will be significantly reduced
