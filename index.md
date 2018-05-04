<!DOCTYPE html>
<html>
	<head>
		<meta http-equiv="Content-Type" content="text/html; charset=utf-8"/>
		<style type="text/css">
		body {background-color:#696969;color:white}
		</style>
		<title>留言板</title>
	</head>
	<body>
		<div><h1>留言板</h1></div>
		<hr width="1500" align="left"/>
		<div id="div1">			
		</div>		
		<div>
			<form>
				<input id="username" type="text"/>
				<br/>
				<p></p>
				<textarea id="message" rows="10" cols="150"/></textarea>				
				<br/>				
			</form>
			<button onclick="publish();">发布</button>
		</div>
		<script>
		var number=1
		function publish()
		{
			
			var message=document.getElementById("message").value;
			var username=document.getElementById("username").value;
			if(message.length!=0){
				if(username.length!=0)
				{
					
					document.getElementById("div1").innerHTML+=number+"# "+username+":"+"<br/>"+message+"<br/>";
					document.getElementById("div1").innerHTML+="<p>_ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ </p>";
					number++;
				}
				else
				{
					document.getElementById("div1").innerHTML+=number+"# 匿名:"+"<br/>"+message+"<br/>";
					document.getElementById("div1").innerHTML+="<p>_ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ __ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ _ </p>";
					number++;
				}
			}			
		}
		</script>
	</body>
</html>
