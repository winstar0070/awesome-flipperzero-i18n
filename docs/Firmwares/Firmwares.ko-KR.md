<h1>Flipper Zero 펌웨어 차이점</h1>
<h3 align="center">
  <a href="Firmwares.md">English</a> | 
  <a href="Firmwares.zh-CN.md">中文</a> | 
  <a href="Firmwares.ja-JP.md">日本語</a> | 
  <a href="Firmwares.ru_RU.md">Русский</a> | 
  <a href="Firmwares.ko-KR.md" style="color: #ffffff;">한국어</a>
</h3>
<h3>
    <code>::</code> 마지막 업데이트 날짜: 2024년 3월 11일. <code>::</code>
</h3>
<p>
    이 문서는 여러
    <a href="#official">Flipper Zero 펌웨어</a> 포크의 차이점을 정리합니다.
</p>
<table>
    <tr>
        <td>
            <strong>다음으로 이동:</strong>
        </td>
        <td><a href="#official">공식</a></td>
        <td><a href="#unleashed">Unleashed</a></td>
        <td><a href="#plugins">RogueMaster</a></td>
        <td><a href="#Xtreme">Xtreme</a></td>
        <td><a href="#Dexv">Xvirus</a></td>
        <td><a href="#SquachWare">SquachWare</a></td>
        <td><a href="#v1nc">v1nc</a></td>
        <td><a href="#wetox">Wetox</a></td>
        <td><a href="#muddledbox">MuddledBox</a></td>
        <td><a href="#summary">요약 (TL;DR)</a></td>
    </tr>
</table>
<h2 id="official">
    ✅ 공식
    <kbd>
        <a href="https://github.com/flipperdevices/flipperzero-firmware">flipperdevices/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>법적 제한으로 인해 지역 고정 Sub-GHz 전송이 있습니다.</li>
    <li>Sub-GHz에서 롤링 코드(동적 암호화)를 저장하고 보내는 기능이 없으며 캡처된 목록에만 표시됩니다.
    </li>
    <li>변경할 수 없는 모든 곳(블루투스 방송, USB 연결 등)에 표시되는 공장 설정 장치 이름입니다.
    </li>
    <ul>
        <li><em>Flipper 팀은 RMA 지원을 쉽게 하기 위해 생산 정보와 연결된 장치 이름 목록을 가지고 있습니다
                    <a href="https://discord.com/channels/740930220399525928/765282833744265246/971881286543224852">(배송 주소 제외)</a>.</em></li>
    </ul>
</ul>
<h2 id="unleashed">
    🔓 Unleashed
    <kbd>
        <a href="https://github.com/DarkFlippers/unleashed-firmware">DarkFlippers/unleashed-firmware</a>
    </kbd>
</h2>
<ul>
    <li><em>UI 변경이 거의 없는 원래 펌웨어 구성 요소의 새로운 기능과 개선에 초점을 맞춘 안정적인 맞춤형 펌웨어</em></li>
    <li>매우 활발한 개발 및 Discord 커뮤니티.</li>
    <li>기본적으로 Sub-GHz 지역 전송 제한을 제거합니다.</li>
    <li><em>dangerous_settings</em> 파일을 통해 Sub-GHz 확장 주파수 범위(예: 레스토랑 호출기)를 허용합니다.</li>
    <li>Settings-&gt;Desktop에서 Flipper 이름을 변경할 수 있습니다.</li>
    <li> <em>setting_user</em> 파일을 사용하지 않고 기본적으로 추가 Sub-GHz 주파수를 추가합니다. <em>setting_user</em>는 사용자 설정에 영향을 주지 않습니다.</li>
    <li> 포함된 dict 파일에 추가 Mifare 클래식 키를 추가하고 사용자 파일은 그대로 둡니다.</li>
    <li>공식 FW에 있지만 잠겨 있는(인코더 코드가 생성되지 않음) 새로운 동적 암호화 프로토콜/롤링 코드를 캡처, 전송 또는 만드는 데 사용할 수 있습니다. <em>(현대식 차고문 등)</em>
    </li>
    <li>Dynamic Sub-GHz 신호 및 코드를 수동으로 추가하여 Flipper를 시스템과 새로운 리모컨으로 페어링할 수 있습니다.</li>
    <li>현재 수정되었거나 새로 추가된 Sub-GHz 프로토콜 목록은 <a
            href="https://github.com/DarkFlippers/unleashed-firmware#current-modified-and-new-subghz-protocols-list">여기에서 확인할 수 있습니다</a>.</li>
    <li>SD 애플리케이션 로더(FAP 파일)를 통해 일반 커뮤니티의 추가 앱과 플러그인이 함께 제공됩니다.
        <ul>
            <li>자세한 내용과 전체 변경 목록은 <a
                    href="https://github.com/DarkFlippers/unleashed-firmware#readme">README</a>에서 확인할 수 있습니다.</li>
        </ul>
</ul>
<h2 id="plugins">
    💫 RogueMaster
    <kbd>
        <a
            href="https://github.com/RogueMaster/flipperzero-firmware-wPlugins">RogueMaster/flipperzero-firmware-wPlugins</a>
    </kbd>
</h2>
<ul>
    <li><a href="#unleashed">Unleashed</a>를 기본 펌웨어로 내장했습니다(<a href="#official">Official</a> 개발자 펌웨어의 포크입니다.)</li>
    <li>Xtreme Settings App의 코드를 크게 덜어내고 CFW Settings로 이름을 바꾼 사본을 포함합니다.</li>
    <li>Patreon에서 비공개 소스 빌드(오픈소스 프로젝트에서 가져온 코드 사용)를 제공합니다.</li>
    <li><em>extend_range.txt</em> 파일을 변경한 후 Sub-GHz 지역 전송 제한을 제거합니다.</li>
<li> <em>extend_range.txt</em> 파일을 통해 Sub-GHz 확장 주파수 범위(예: 식당 호출기)를 허용합니다.</li>
    <li>에는 Sub-GHz 프로토콜이 있으며 Unleashed FW에서 가져온 대부분의 다른 변경 사항이 있습니다(<a href="#unleashed">changes</a> 참조).</li>
    <li> 추가 커스텀 자산 <em>를 추가합니다(Mifare 클래식 사전, 예제 파일 등)</em>.</li>
    <li>공식 펌웨어(미완성, WIP) <em>(블리딩 에지)</em>에 아직 병합되지 않은 공식 펌웨어의 일부 PR이 포함되어 있습니다.
    </li>
    <li>실험적인 "게임 전용 모드"(일명 멍청한 모드)가 포함되어 있습니다.</li>
    <li>향상되었지만 실험적인 새로운 "돌핀 레벨" 시스템이 포함되어 있습니다.</li>
    <li>SD 애플리케이션 로더(FAP 파일)를 통해 일반 커뮤니티의 추가 앱과 플러그인을 포함합니다.</li>
    <li>또한 기타 여러 가지 작은 조정, 변경 사항 및 수많은 추가 애니메이션이 포함되어 있습니다.</li>
    <ul>
        <li>자세한 내용과 전체 목록은 <a
                href="https://github.com/RogueMaster/flipperzero-firmware-wPlugins#readme">README</a>를 참조하세요.</li>
    </ul>
</ul>
<h2 id="Xtreme">
    💋 Xtreme
    <kbd>
        <a href="https://github.com/Flipper-XFW/Xtreme-Firmware">Flipper-XFW/Xtreme-Firmware</a>
    </kbd>
</h2>
<ul>
    <li>원래 RogueMaster를 기반으로 만들어졌으며, 이후 향후 개발을 위해 <a href="#unleashed">Unleashed</a> + <a href="#official">Official</a> FW의 포크로 전환되었습니다.</li>
    <li>커스텀 UI 및 커스텀 메인 메뉴 테마와 자산 팩(아이콘, 애니메이션)을 추가합니다.</li>
    <li>기본적으로 Sub-GHz 지역 전송 제한을 제거합니다.</li>
    <li> Xtreme 설정 앱을 통해 Sub-GHz 확장 주파수 범위(예: 레스토랑 호출기)를 허용합니다.</li>
    <li>Xtreme 설정 앱을 통해 Flipper의 이름을 변경할 수 있습니다.</li>
    <li>Sub-GHz 프로토콜과 대부분의 다른 변경 사항은 Unleashed FW에서 가져왔습니다(<a href="#unleashed">변경 사항</a> 참조).</li>
    <li>추가 커스텀 자산<em>(Mifare Classic dict, 별도 설치되는 추가 애니메이션, 예제 파일 등)</em>을 추가합니다.</li>
    <li>RogueMaster와 유사한 향상된 "Dolphin Level" 시스템을 포함합니다.</li>
    <li>SD 애플리케이션 로더(FAP 파일)를 통해 일반 커뮤니티의 추가 앱과 플러그인을 포함합니다.</li>
    <li>또한 기타 여러 가지 작은 조정, 변경 사항 및 안정성 수정 사항이 포함되어 있습니다.</li>
</ul>
<h2 id="Dexv">
    ❌Xvirus
    <kbd>
        <a href="https://github.com/Xvirus-Team/xvirus-firmware">Xvirus-Team/xvirus-firmware</a>
    </kbd>
</h2>
<ul>
    <li><a href="#unleashed">Unleashed FW</a>의 포크입니다.</li>
    <li>공식 펌웨어에 포함되지 않은 커스텀 테마 그래픽을 추가합니다.</li>
    <li><em>extend_range.txt</em> 파일을 변경한 후 Sub-GHz 지역 전송 제한을 제거합니다.</li>
    <li><em>extend_range.txt</em> 파일을 통해 Sub-GHz 확장 주파수 범위(예: 식당 호출기)를 허용합니다.</li>
    <li>Sub-GHz 프로토콜과 대부분의 다른 변경 사항은 Unleashed FW에서 가져왔습니다(<a href="#unleashed">변경 사항</a> 참조).</li>
    <li>추가 커스텀 자산<em>(Mifare Classic dict, 예제 파일 등)</em>을 추가합니다.</li>
    <li>SD 애플리케이션 로더(FAP 파일)를 통해 일반 커뮤니티의 추가 앱과 플러그인을 포함합니다.</li>
</ul>
<h2 id="SquachWare">
    🌲 SquachWare
    <kbd>
        <a href="https://github.com/skizzophrenic/SquachWare-CFW">skizzophrenic/SquachWare-CFW</a>
    </kbd>
</h2>
<ul>
    <li><em>(OEM+)</em></li>
    <li><em>SquachWare는 당분간 포기되었습니다! 아직 좋은 파일이 몇 개 있지만 기본 펌웨어가 매우 오래되었습니다!! 나중에 프로젝트를 부활시키고 싶지만 지금은 중단 상태입니다!</em></li>
    <li>커스텀 애니메이션/분위기를 추가합니다.</li>
    <li>내장 이름 변경 기능이 포함되어 있습니다! (장치 이름을 변경하기 위해 다시 컴파일할 필요가 없습니다).</li>
    <li>SD 애플리케이션 로더(FAP 파일)를 통해 추가 커뮤니티 기반 앱 및 플러그인을 포함합니다.</li>
    <li>커뮤니티 기반 BadUSB 스크립트를 포함합니다.</li>
    <li>커뮤니티 기반 Sub-GHz 파일을 포함합니다.</li>
            <ul>
            <li>자세한 내용은 <a
                    href="https://github.com/skizzophrenic/SquachWare-CFW">README</a>에서 확인할 수 있습니다.</li>
        </ul>
</ul>
<h2 id="v1nc">
    ⌨v1nc
    <kbd>
        <a href="https://github.com/v1nc/flipperzero-firmware">v1nc/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>스크립트 키워드 <code>DUCKY_LANG</code>를 통해 Duckyscripts의 여러 키보드 레이아웃을 지원합니다.</li>
    <li>업스트림 Unleashed 펌웨어가 오래되어 유지 관리되지 않는 것 같습니다.</li>
    <li>일부 통합 커뮤니티 플러그인 및 게임이 포함되어 있지만 업데이트되지 않은 FAP 로더.</li>
</ul>
<h2 id="wetox">
    🎩 Wetox
    <kbd>
        <a href="https://github.com/wetox-team/flipperzero-firmware">wetox-team/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>dev 브랜치는 공개적으로 사용하도록 고안된 반면, 다른 브랜치는 해커톤 제출물을 테스트하거나 보관하는 데 사용됩니다.
    </li>
    <li>업스트림 공식 펌웨어가 오래되어 유지 관리되지 않는 것 같습니다.</li>
    <li>사전 공격을 통해 T5577 RFID 비밀번호를 크래킹합니다.</li>
    <li>데스크탑 헤더 브랜딩 [WTX].</li>
    <li>다른 <a
            href="https://github.com/wetox-team/flipperzero-firmware/branches">브랜치</a>에서 자주 업데이트되는 흥미로운 실험 내용이 있습니다.</li>
</ul>
<h2 id="muddledbox">
    📦 머들드박스
    <kbd>
        <a href="https://github.com/MuddledBox/flipperzero-firmware">MuddledBox/flipperzero-firmware</a>
    </kbd>
</h2>
<ul>
    <li>현재 폐기된 최초의 '맞춤형 펌웨어'입니다.</li>
    <li>Sub-GHz 지역 전송 제한을 제거합니다.</li>
    <li>설정의 정보 페이지에 자체 홍보 이미지를 추가합니다.</li>
    <li> 캡처할 몇 가지 공통 Sub-GHz 주파수를 추가합니다.</li>
</ul>
<h2 id="summary">
    📝 요약
    <kbd>(TL;DR)</kbd>
</h2>
<ul>
    <li>업스트림(공식) 펌웨어를 최신 상태로 유지하는 것이 중요합니다.</li>
    <li>TX 제한 제거는 대부분의 상황에서 불법입니다. 사용에 따른 책임은 사용자 본인에게 있습니다.</li>
    <li>MuddledBox는 최초의 인기 있는 펌웨어 포크였지만 성장하지는 못했습니다.</li>
    <li>Unleashed는 핵심 기능, 안정성 및 Sub-GHz 프로토콜에 더 중점을 둡니다.</li>
    <li>Xtreme은 새로운 시각적 조정, UI 커스텀 등에 더 중점을 둡니다.</li>
    <li>RogueMaster는 Unleashed를 기반으로 하지만 일부 상황에서는 Unleashed보다 안정성이 떨어질 수 있습니다.</li>
    <li>SquachWare는 OFW에서 분기되어 OFW의 안전성과 편의성을 유지하면서 바로 사용할 수 있는 많은 커스텀 요소를 추가합니다.</li>
</ul>
