<script setup>
	defineProps({
		message: String
	})
</script>
<template>
	<button class="btn"><span>{{ message }}</span></button>
</template>
<script>
	window.addEventListener('load', ()=> {
		const startIcon = document.querySelectorAll('.btn[startIcon]')
		const endIcon = document.querySelectorAll('.btn[endIcon]')
		
		const setIcon = function(type, iconName, element) {
			const icon = document.createElement('i')
				icon.classList.add('fa-solid')
			const span = document.createElement('span')
				span.innerHTML = 'Default'
				span.style.display = 'inline-block'
			// <i class="fa-solid fa-cart-shopping"></i>
			icon.classList.add(iconName)
	
			if (type == 'start') {
				// let principalChild = startIcon.childNodes[0]
				span.style.marginLeft = '.5em'
				element.appendChild(icon)
				element.appendChild(span)
			} else {
				span.style.marginRight = '.5em'
				element.appendChild(span)
				element.append(icon)
			}
		}
			 
		if (startIcon) {
			console.log('empieza: ', startIcon)
			startIcon.forEach(element => {
				setIcon('start', element.getAttribute('startIcon'), element)
			})
		}
		if(endIcon) {
			console.log('termina: ', endIcon)
			endIcon.forEach(elemento => {
				setIcon('end', elemento.getAttribute('endIcon'), elemento)
			})
		}
	})
</script>

<style scoped>
	.btn {
		box-shadow: 0px 2px 3px rgba(51, 51, 51, 0.2);
	    border-radius: 6px;
	    padding: 8px 20px;
	    font-size: 14px;
	    font-weight: 500;
	    line-height: 20px;
	    text-align: center;
	    outline: none;
	    border: none;
		width: fit-content;
		transition: all .2s;
	}
	button[color="default"] {
		background: #E0E0E0;		
		color: #3F3F3F;		
	}
	button[color="default"].hover, button[color="default"]:hover, button[color="default"]:focus {
		background: #AEAEAE;
	}
	button[variant='outline'] {
		border: 1px solid #3D5AFE;
		color: #3D5AFE;
		background:#fff;
	}
	button[variant='outline'].hover, button[variant='outline']:hover, button[variant='outline']:focus {
		background: rgba(41, 98, 255, 0.1)
	}
	button[variant='text'] {
		background: transparent;
		color: #3D5AFE;
	}
	button[variant='text'].hover, button[variant='text']:hover, button[variant='text']:focus {
		background: rgba(41, 98, 255, 0.1)
	}
	button[disableShadow] {
		box-shadow: unset;
	}
	button[disabled] {
		color: #9E9E9E;
	}
	button[size="sm"] {
		height: 32px;
	}
	button[size="md"] {
		height: 36px;
	}
	button[size="lg"] {
		height: 42px;
	}
	button[color="primary"] {
		background: #2962FF;
		color: #fff;
	}
	button[color="primary"].hover, button[color="primary"]:hover, button[color="primary"]:focus {
		background: #0039CB;
	}
	button[color="secondary"] {
		color: #fff;
		background: #455A64;
	}
	button[color="secondary"].hover, button[color="secondary"]:hover, button[color="secondary"]:focus {
		background: #1C313A;
	}
	button[color="danger"] {
		background: #D32F2F;
		color: #fff;
	}
	button[color="danger"].hover, button[color="danger"]:hover, button[color="danger"]:focus {
		background: #9A0007;
	}
</style>