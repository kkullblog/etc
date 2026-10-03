<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>FTP Rush 3.66 FTPS/SFTP 클라우드 스토리지 클라이언트 사용법 완벽 가이드</title>
    <style>
        body {
            font-family: 'Apple SD Gothic Neo', 'Malgun Gothic', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 850px;
            margin: 40px auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .post-container {
            background: #fff;
            padding: 40px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.05);
        }
        h1 {
            font-size: 26px;
            color: #2c3e50;
            margin-bottom: 20px;
            border-bottom: 2px solid #3498db;
            padding-bottom: 10px;
        }
        h2 {
            font-size: 20px;
            color: #2980b9;
            margin-top: 35px;
            margin-bottom: 15px;
        }
        h3 {
            font-size: 16px;
            color: #34495e;
            margin-top: 20px;
            margin-bottom: 10px;
        }
        p {
            margin-bottom: 15px;
            font-size: 15px;
        }
        .step-box {
            background: #f8f9fa;
            border-left: 4px solid #3498db;
            padding: 15px 20px;
            margin: 20px 0;
            border-radius: 0 4px 4px 0;
        }
        ul {
            margin-bottom: 15px;
            padding-left: 25px;
        }
        li {
            margin-bottom: 8px;
            font-size: 15px;
        }
        .tip {
            background: #e8f4fd;
            border: 1px solid #bbe1fa;
            padding: 15px;
            border-radius: 6px;
            margin: 20px 0;
        }
        code {
            background: #eee;
            padding: 2px 6px;
            border-radius: 4px;
            font-family: monospace;
            font-size: 14px;
            color: #c7254e;
        }
        /* 반응형 이미지 스타일 */
        .post-image-wrap {
            text-align: center;
            margin: 20px 0;
        }
        .post-image-wrap img {
            max-width: 100%;
            height: auto;
            border-radius: 6px;
            box-shadow: 0 2px 8px rgba(0,0,0,0.1);
            border: 1px solid #e1e1e1;
        }
        @media (max-width: 768px) {
            body {
                padding: 10px;
                margin: 10px auto;
            }
            .post-container {
                padding: 20px;
            }
            h1 {
                font-size: 22px;
            }
            h2 {
                font-size: 18px;
            }
        }
    </style>
</head>
<body>
<div class="post-container">
    <h1>FTP Rush 3.66 FTPS/SFTP 클라우드 스토리지 클라이언트 사용법 총정리</h1>
    
    <p>안녕하세요! 오늘은 대용량 파일 전송과 멀티 세션 처리에 뛰어난 고성능 FTP/SFTP 클라이언트인 <strong>FTP Rush</strong>의 사용법을 상세히 알아보겠습니다. 초보자분들도 쉽게 따라 하실 수 있도록 화면 구성과 접속 설정, 파일 전송 방법까지 단계별로 정리해 드립니다.</p>

    <hr style="border:0; border-top:1px solid #eee; margin:30px 0;">

    <h2>1. 프로그램 첫 실행 및 인터페이스 구성</h2>
    <p>FTP Rush를 처음 실행하면 아래와 같은 깔끔한 듀얼 패널 인터페이스가 반겨줍니다. 좌측은 원격 서버, 우측은 내 컴퓨터(로컬)의 파일 구조를 한눈에 비교하고 관리할 수 있도록 설계되어 있습니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://kkull.blog.fc2.com/img/u11.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/u11.jpg" alt="FTP Rush 메인 실행 화면 및 상단 접속 바"></a>
    </div>

    <ul>
        <li><strong>상단 접속 바:</strong> 프로토콜, 암호화 방식, 호스트 주소, 포트, 사용자 이름, 암호를 곧바로 입력하여 빠른 접속을 수행할 수 있습니다.</li>
        <li><strong>좌측 패널 (서버):</strong> 접속한 원격 FTP 서버의 디렉토리 및 파일 목록이 표시됩니다.</li>
        <li><strong>우측 패널 (로컬):</strong> 현재 작업 중인 내 PC의 로컬 디렉토리 경로와 파일들이 표시됩니다.</li>
    </ul>

    <h2>2. 사이트 관리자를 통한 서버 등록 및 연결 설정</h2>
    <p>매번 접속 정보를 입력하기 번거롭다면 <strong>사이트 관리자</strong> 기능을 통해 주소와 계정을 미리 저장해 둘 수 있습니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://kkull.blog.fc2.com/img/u22.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/u22.jpg" alt="사이트 관리자 설정 창 (호스트, 포트, 계정 정보 입력)"></a>
    </div>

    <div class="step-box">
        <h3>📌 사이트 등록 순서</h3>
        <ul>
            <li>상단 메뉴에서 <strong>사이트 관리자</strong> 아이콘을 클릭합니다.</li>
            <li>원하는 폴더 위치(예: <code>FTPRush 사이트</code> 등)를 선택하고 하단의 <code>+</code> 버튼을 눌러 새 사이트를 추가합니다.</li>
            <li><strong>호스트:</strong> 접속할 서버 주소 입력 (예: <code>kkull.ipdisk.co.kr</code>)</li>
            <li><strong>포트:</strong> 포트 번호 입력 (<code>25</code>)</li>
            <li><strong>사용자 이름 및 암호:</strong> 발급받은 계정 정보 입력 후 <strong>연결</strong> 버튼 클릭</li>
        </ul>
    </div>

    <h2>3. 서버 폴더 탐색 및 디렉토리 구조 확인</h2>
    <p>서버에 정상적으로 로그인되면, 좌측 서버 패널에 원격 저장소의 드라이브 및 폴더 목록이 나타납니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://kkull.blog.fc2.com/img/u33.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/u33.jpg" alt="서버 로그인 성공 후 HDD2 및 Horror 폴더 목록 표시 화면"></a>
    </div>

    <p>서버 패널에 표시된 폴더(예: <code>HDD2/</code> -&gt; <code>Horror/</code> 등)를 더블클릭하면 하위 디렉토리로 부드럽게 진입할 수 있으며, 하단 로그 창을 통해 접속 상태와 디렉토리 목록 불러오기 성공 여부를 실시간으로 확인할 수 있습니다.</p>

    <h2>4. 파일 전송(다운로드 / 업로드) 방법</h2>
    <p>FTP Rush는 드래그 앤 드롭뿐만 아니라 직관적인 마우스 우클릭 메뉴를 통해 간편하게 파일을 주고받을 수 있습니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://kkull.blog.fc2.com/img/u44.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/u44.jpg" alt="파일 우클릭 전송 메뉴 및 하단 전송 진행 상태 바"></a>
    </div>

    <div class="step-box">
        <h3>📌 파일 전송(다운로드) 진행하기</h3>
        <ul>
            <li>서버 패널에서 전송(다운로드)하고자 하는 파일을 선택합니다 (예: 동영상 파일 등).</li>
            <li>마우스 우클릭을 한 뒤 <strong>전송 (Ctrl + T)</strong> 메뉴를 클릭합니다.</li>
            <li>우측 로컬 경로로 파일이 즉시 다운로드되며, 하단 상태 바에서 전송 속도, 용량, 진행률을 모니터링할 수 있습니다.</li>
        </ul>
    </div>
<li>&nbsp;<a href="https://www.wftpserver.com/download/FTPRush.zip">Download (포터블)</a></li>
    <div class="tip">
        <strong>💡 Tip:</strong> FTP Rush는 멀티 스레드 전송을 지원하여 대용량 파일도 끊김 없이 안정적으로 고속 전송이 가능합니다. 
    </div>

    <hr style="border:0; border-top:1px solid #eee; margin:30px 0;">
    <p style="text-align: center; color: #777; font-size: 14px;">© Dozil | Retrospect</p>
</div>
</body>
</html>
