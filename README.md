(function autoClick() {
    const targetSelector = '.relative.w-24.h-16.rounded-full.cursor-pointer';
    const checkInterval = 2000; // Check every 2 seconds

    function checkAndClick() {
        const target = document.querySelector(targetSelector);

        if (target) {
            console.log("Target found!");

            const img = target.querySelector('img[alt="Circle Image"]');
            if (img && img.classList.contains("brightness-0") && img.classList.contains("invert")) {
                console.log("Not connected! Clicking...");
                target.click();
            } else {
                console.log("Already connected.");
            }
        } else {
            console.log("Target not found.");
        }
    }

    setInterval(checkAndClick, checkInterval);
})();
