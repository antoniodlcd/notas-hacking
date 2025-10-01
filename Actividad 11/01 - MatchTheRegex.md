## Descripción
How about trying to match a regular expression. The website is running [here](http://saturn.picoctf.net:54395/).
## Solución
en el código fuente de la página, el script viene así:
```
function send_request() {
	let val = document.getElementById("name").value;
	// ^p.....F!?
	fetch(`/flag?input=${val}`)
		.then(res => res.text())
		.then(res => {
			const res_json = JSON.parse(res);
			alert(res_json.flag)
			return false;
		})
	return false;
}
```
significa que recibe un valor y lo valida. El mismo script tiene un comentario con una pista, por lo que le inserté la palabra "picoCTF" y me dio la bandera "picoCTF{succ3ssfully_matchtheregex_8ad436ed}"
## Notas
## Referencias
