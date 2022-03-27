# VanillaJS - Ajax

```
var x = new XMLHttpRequest()
  x.open('GET','get.php',false)
  x.onload = function () {
    if(x.status >= 200 && x.status < 300){
      if(x.responseText.length > 0){
        // do something
        }
      }

    }
  }
  x.send()
```

# Promises

```
function iniDulu(){
  return new Promise(function (resolve,reject) {
    var x = new XMLHttpRequest()
    x.open('GET', 'get.php', false)
    x.onload = function () {
      if (x.status >= 200 && x.status < 300) {
          // do something
          resolve()
        }
      } else {
        reject(new Error(x.responseText))
      }
    }
    x.send()
  })
}

function baruItu(){}

iniDulu().then(baruItu())
```

# Instant Get JSON

```
let url = 'https://www.example.com'
fetch(url).then(res => res.json())
.then(out => console.log(out))
.catch(err => throw err)

// Or 

let fetchRes = fetch(url)
fetchRes.then(res => res.json()).then(out => {
 console.log(out)
})
```

 

