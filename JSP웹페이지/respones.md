# 전체코드
<details> <summary>코드</summary> 
	
	    <%@ page language="java" contentType="text/html; charset=UTF-8"
	    pageEncoding="UTF-8"%>
	    <! DOCTYPE html>
	    <html>
	    <head>
	    <meta charset="UTF-8">
	    <title>내장객체 - request</title>
	    </head>
	    <body>
	    	<%
	    		request.setCharacterEncoding("UTF-8");
	    		String id = request.getParameter("id");
	    		String pw = request.getParameter("pw");
	    		
	    		if( id.equals("joeun") && pw.equals("123456") ) {
	    			// 리다이렉트 방식으로 페이지 이동
	    			response.sendRedirect("response.jsp");
	    			}else {
	    			response.sendRedirect("response.jsp");
	    			}
	    	%>
			
	</body>
	</html>
</details>

# 전체코드
    <%@ page language="java" contentType="text/html; charset=UTF-8"
        pageEncoding="UTF-8"%>
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="UTF-8">
    <title>내장객체 request</title>
    </head>
    <body>
    	<h1>로그인</h1>
    	<form action="Main.jsp">
    		<p>
    			<label for = "id">아이디: </label>
    			<input type="text" name = "id" id = "id">
    		</p>
    		
    		<p>
    			<label for = "pw">비밀번호: </label>
    			<input type="text" name = "pw" id = "pw">
    		</p>
    		<input type="submit" value="로그인">
    	</form>
    </body>
    </html>

# 전체코드 
    <%@ page language="java" contentType="text/html; charset=UTF-8"
        pageEncoding="UTF-8"%>
    <!DOCTYPE html>
    <html>
    <head>
    <meta charset="UTF-8">
    <title>로그인 성공</title>
    </head>
    <body>
    	<h1>로그인 성공</h1>
    
    </body>
    </html>
