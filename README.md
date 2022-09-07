# RandomTikTok
# https://zacharygopinath.github.io/RandomTikTok/

- TikTok link contains 'https://vm.tiktok.com/' then 9 alphanumeric characters (0-9, a-z/A-Z)
- Randomly generate the 9 character ending
```
const chars = [
            '0', '1', '2', '3', '4', '5', '6', '7', '8', '9',
            'a', 'b', 'c', 'd', 'e','f', 'g', 'h', 'i', 'j', 
            'k', 'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 
            'u', 'v', 'w', 'x', 'y', 'z'
];
const linkBase = 'https://vm.tiktok.com/';
let randomLink = '';
let random = '';

for (let i = 9; i > 0; i--) {             
    random = chars[Math.floor(Math.random() * 35)];

    if (random.toUpperCase() != random.toLowerCase()){ // check if is letter
        if (Math.floor(Math.random() * 2) == 1) { // 50/50 to capitalize
            random = random.toUpperCase();
        }
    }
    randomLink += random;
}
```
- This might not always create a working link
- TikTok automatically redirects invalid links to a random video
