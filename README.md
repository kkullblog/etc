<html lang="ko">
<head>
    <meta charset="UTF-8">
    <title>corgiplayer - 안드로이드 네트워크 비디오 플레이어 앱 사용법 (FTP, SMB, WebDAV 지원)</title>
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
            border-bottom: 2px solid #e67e22;
            padding-bottom: 10px;
        }
        h2 {
            font-size: 20px;
            color: #d35400;
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
            background: #fdfefe;
            border-left: 4px solid #e67e22;
            border: 1px solid #f5cba7;
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
            background: #fef5e7;
            border: 1px solid #f8c471;
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
        .post-image-wrap {
            text-align: center;
            margin: 25px 0;
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
    <h1>corgiplayer - 안드로이드 네트워크 스트리밍 비디오 플레이어 앱 사용법 완벽 가이드</h1>
    
    <p>안녕하세요! 오늘은 NAS나 홈 서버, 원격 FTP/SMB/SFTP/WebDAV 서버에 저장된 동영상을 스마트폰에서 간편하게 스트리밍하고 재생할 수 있는 모바일 전용 고성능 미디어 플레이어인 <strong>corgiplayer</strong>(코기플레이어) 앱의 사용법을 자세히 알아보겠습니다.</p>

    <hr style="border:0; border-top:1px solid #eee; margin:30px 0;">

    <h2>1. corgiplayer 주요 특징 및 앱 개요</h2>
    <p>corgiplayer는 깔끔한 UI와 직관적인 제스처 컨트롤을 제공하며, 다양한 네트워크 프로토콜을 완벽하게 지원하는 스마트폰 최적화 비디오 플레이어입니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv2.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv2.jpg" alt="corgiplayer 구글 플레이스토어 소개 및 주요 기능"></a>
    </div>

    <ul>
        <li><strong>폭넓은 프로토콜 지원:</strong> WebDAV, SMB, FTP, SFTP 등 다양한 네트워크 연결 방식을 지원하여 원격 저장소에 쉽게 접근할 수 있습니다.</li>
        <li><strong>로컬 및 네트워크 재생:</strong> 스마트폰 내부에 저장된 로컬 파일 재생뿐만 아니라 외부 서버 스트리밍에 최적화되어 있습니다.</li>
        <li><strong>편리한 제스처 컨트롤:</strong> 화면 밝기, 볼륨 조절, 탐색 등을 화면 터치 제스처로 쾌적하게 제어할 수 있습니다.</li>
    </ul>

    <h2>2. 네트워크 연결 추가 및 설정 방법 (FTP 기준)</h2>
    <p>앱 하단의 <strong>네트워크</strong> 탭으로 이동한 뒤, 우측 하단의 <code>+</code> 버튼을 누르면 SMB, SFTP, FTP, WebDAV, URL 열기 등 다양한 연결 방식을 선택할 수 있습니다.</p>
    
    <div class="post-image-wrap">
        <a href="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv5.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv5.jpg" alt="네트워크 탭에서 FTP, SMB 등 프로토콜 추가 메뉴 화면"></a>
    </div>

    <p>FTP 연결을 선택하면 연결 이름과 최종 접속 URL을 입력하는 화면이 나타납니다. 서버 주소와 포트 번호, 경로를 정확히 입력합니다.</p>

    <div class="post-image-wrap">
        <a href="https://blog-imgs-160.fc2.com/k/k/u/kkull/v77.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/v77.jpg" alt="FTP 연결 추가 및 최종 접속 URL 설정 화면"></a>
    </div>

    <div class="step-box">
        <h3>📌 FTP 연결 설정 순서</h3>
        <ul>
            <li><strong>연결 이름:</strong> 구분을 위한 별칭 입력 (예: <code>Horror</code> 등)</li>
            <li><strong>최종 접속 URL:</strong> 예시처럼 프로토콜과 주소, 포트, 폴더 경로 입력 (예: <code>ftp://kkull.ipdisk.co.kr:25/HDD2</code>)</li>
            <li><strong>연결 테스트:</strong> 하단의 <strong>연결 테스트</strong> 버튼을 눌러 정상 작동 여부를 확인합니다.</li>
        </ul>
    </div>

    <h2>3. 사용자 계정 인증 및 로그인</h2>
    <p>연결 테스트가 성공하거나 다음 단계로 넘어가면, 서버에 접근하기 위한 사용자 인증 정보를 입력하는 창이 나옵니다.</p>
    
    <div class="post-image-wrap">
     <a href="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv4.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv4.jpg" alt="FTP 연결 수정 및 사용자 이름, 비밀번호 입력 화면"></a>
    </div>

    <ul>
        <li><strong>사용자 이름:</strong> 서버에 등록된 계정 ID 입력 (예: <code>gold</code>)</li>
        <li><strong>비밀번호:</strong> 해당 계정의 비밀번호 입력 후 <strong>다음</strong> 또는 <strong>추가</strong>를 누르면 등록이 완료됩니다.</li>
    </ul>


 <h2>4. FTP 연결 및 이름 설정</h2>
    <p>사용자 정보를 입력후에 연결이름을 작성해줍니다.자연스럽게(?)Horror로 해보겠습니다.작성후 연결테스트를 누른후 추가해 줍니다..</p>
    
    <div class="post-image-wrap">
     <a href="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv6.jpg/" target="_blank"><img src="https://blog-imgs-160.fc2.com/k/k/u/kkull/vv6.jpg" alt="FTP 연결 수정 및 사용자 이름, 비밀번호 입력 화면"></a>
    </div>

    <div class="tip">
        <strong>💡 Tip:</strong> 추가로 등록된 네트워크 서버들은 메인 네트워크 화면에 카드 형태로 깔끔하게 정렬되며, 언제든지 우측 메뉴 버튼을 통해 설정을 수정하거나 삭제할 수 있습니다. 스마트폰으로 홈 서버나 NAS의 영상들을 쉽고 빠르게 즐겨보세요!
    </div>

    <hr style="border:0; border-top:1px solid #eee; margin:30px 0;">
    <p style="text-align: center; color: #777; font-size: 14px;">© Dozil | Retrospect</p>
</div>
</body>
</html>
