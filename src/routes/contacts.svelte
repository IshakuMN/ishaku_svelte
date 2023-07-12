<script>
	import github from '$lib/images/github.svg';
	import email from '$lib/images/mail-svgrepo-com.svg';
	import telegram from '$lib/images/telegram-svgrepo-com.svg';
	import linkedIn from '$lib/images/linkedin-svgrepo-com.svg';
</script>

<div class="icon-container">
	<div>
		<a href="https://github.com/IshakuMN">
			<img id="gh-link" src={github} alt="Github" />
		</a>
	</div>
	<div>
		<a href="mailto:ishakumarch@gmail.com">
			<img id="email" src={email} alt="email" />
		</a>
	</div>
	<div>
		<a href="https://t.me/ishakumn">
			<img id="tg-link" src={telegram} alt="" />
		</a>
	</div>
	<div>
		<a href="https://www.linkedin.com/in/ishakumn">
			<img id="linkedin" src={linkedIn} alt="" />
		</a>
	</div>
</div>

<style>
	.icon-container {
		display: flex;
		flex-direction: column;
		justify-content: flex-start;
		align-items: flex-end;
		margin-top: 20px;
		margin-right: 20px;
		position: static;
	}

	#email {
		width: 30;
		height: 30px;
	}
	#email:hover {
		filter: invert(0.5);
	}

	#gh-link {
		width: 30px;
		height: 30px;
	}

	#gh-link:hover {
		filter: invert(0.5);
	}

	#linkedin {
		width: 30px;
		height: 30px;
	}

	#linkedin:hover {
		filter: invert(0.5);
	}
	#tg-link {
		width: 30px;
		height: 30px;
	}
	#tg-link:hover {
		filter: invert(0.5);
	}
</style>
