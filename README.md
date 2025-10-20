<!DOCTYPE html>
<html lang="ko">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>에브라임 스터디카페 - 직영점 문의</title>
    <script src="https://cdn.tailwindcss.com"></script>
</head>
<body class="min-h-screen bg-gradient-to-br from-blue-50 to-indigo-100 p-4">
    <div class="max-w-2xl mx-auto">
        <div class="bg-white rounded-t-2xl shadow-lg p-6 mt-8">
            <h1 class="text-3xl font-bold text-center text-indigo-900">에브라임 스터디카페</h1>
            <p class="text-center text-gray-600 mt-2">직영점 문의 시스템</p>
        </div>

        <div id="page-branch" class="bg-white rounded-b-2xl shadow-lg p-6">
            <h2 class="text-xl font-semibold text-gray-800 mb-4">직영점을 선택해주세요</h2>
            <div class="space-y-3">
                <button onclick="selectBranch('gyeyang', '인천계양본점', '🏢')" class="w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between">
                    <span class="text-lg font-medium">인천계양본점</span>
                    <span class="text-2xl">🏢</span>
                </button>
                <button onclick="selectBranch('bakchon', '인천박촌역점', '🚇')" class="w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between">
                    <span class="text-lg font-medium">인천박촌역점</span>
                    <span class="text-2xl">🚇</span>
                </button>
                <button onclick="selectBranch('bupyeong', '부평삼산점', '🏙️')" class="w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between">
                    <span class="text-lg font-medium">부평삼산점</span>
                    <span class="text-2xl">🏙️</span>
                </button>
                <button onclick="selectBranch('sangdong', '부천상동점', '🏪')" class="w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between">
                    <span class="text-lg font-medium">부천상동점</span>
                    <span class="text-2xl">🏪</span>
                </button>
                <button onclick="selectBranch('sinjung', '부천신중동점', '🏬')" class="w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between">
                    <span class="text-lg font-medium">부천신중동점</span>
                    <span class="text-2xl">🏬</span>
                </button>
            </div>
        </div>

        <div id="page-type" class="bg-white rounded-b-2xl shadow-lg p-6 hidden">
            <button onclick="goToPage('branch')" class="flex items-center text-indigo-600 hover:text-indigo-800 mb-4">
                <svg class="w-5 h-5 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                </svg>
                직영점 다시 선택
            </button>
            <div class="bg-indigo-50 rounded-lg p-3 mb-4">
                <p class="text-sm text-indigo-800">선택한 지점: <span id="selected-branch-name" class="font-semibold"></span></p>
            </div>
            <h2 class="text-xl font-semibold text-gray-800 mb-4">무엇을 도와드릴까요?</h2>
            <div id="inquiry-types" class="space-y-3"></div>
            <button onclick="goToPage('branch')" class="w-full mt-4 bg-gray-200 hover:bg-gray-300 text-gray-700 font-semibold py-3 px-6 rounded-lg shadow-md transition-all">
                취소
            </button>
        </div>

        <div id="page-parking-info" class="bg-white rounded-b-2xl shadow-lg p-6 hidden">
            <button onclick="goToPage('type')" class="flex items-center text-indigo-600 hover:text-indigo-800 mb-4">
                <svg class="w-5 h-5 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                </svg>
                뒤로가기
            </button>
            <div class="bg-blue-50 border-l-4 border-blue-500 p-6 rounded-lg">
                <div class="flex items-start">
                    <span class="text-4xl mr-4">🅿️</span>
                    <div>
                        <h3 class="text-xl font-bold text-blue-900 mb-3">부평삼산점 주차 안내</h3>
                        <p class="text-gray-700 text-lg leading-relaxed">
                            아파트 상가에 주차가 가능하지만, 안되는 경우도 있으니 참고해주시기 바랍니다.
                        </p>
                    </div>
                </div>
            </div>
            <div class="flex gap-3 mt-6">
                <button onclick="goToPage('type')" class="flex-1 bg-gray-200 hover:bg-gray-300 text-gray-700 font-semibold py-3 px-6 rounded-lg shadow-md transition-all">
                    취소
                </button>
                <button onclick="goToPage('branch')" class="flex-1 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white font-semibold py-3 px-6 rounded-lg shadow-md transition-all">
                    처음으로
                </button>
            </div>
        </div>

        <div id="page-form" class="bg-white rounded-b-2xl shadow-lg p-6 hidden">
            <button onclick="goToPage('type')" class="flex items-center text-indigo-600 hover:text-indigo-800 mb-4">
                <svg class="w-5 h-5 mr-1" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                    <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7"></path>
                </svg>
                문의 유형 다시 선택
            </button>
            <div class="bg-indigo-50 rounded-lg p-3 mb-4 space-y-1">
                <p class="text-sm text-indigo-800">지점: <span id="form-branch-name" class="font-semibold"></span></p>
                <p class="text-sm text-indigo-800">문의 유형: <span id="form-type-name" class="font-semibold"></span></p>
            </div>
            <h2 class="text-xl font-semibold text-gray-800 mb-4">
                <span id="form-type-icon"></span> <span id="form-type-title"></span>
            </h2>
            <div class="space-y-4">
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">좌석 번호</label>
                    <input type="text" id="seat-number" placeholder="예: 42" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent">
                </div>
                <div>
                    <label class="block text-sm font-medium text-gray-700 mb-2">문의 내용</label>
                    <textarea id="inquiry-content" placeholder="문의하실 내용을 상세히 입력해주세요" rows="6" class="w-full px-4 py-3 border border-gray-300 rounded-lg focus:ring-2 focus:ring-indigo-500 focus:border-transparent resize-none"></textarea>
                </div>
                <div id="error-message" class="bg-red-50 border border-red-200 rounded-lg p-3 items-center text-red-700 hidden">
                    <svg class="w-5 h-5 inline mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 8v4m0 4h.01M21 12a9 9 0 11-18 0 9 9 0 0118 0z"></path>
                    </svg>
                    <span>문의 접수에 실패했습니다. 다시 시도해주세요.</span>
                </div>
                <div id="success-message" class="bg-green-50 border border-green-200 rounded-lg p-3 items-center text-green-700 hidden">
                    <span>✅ 문의가 성공적으로 접수되었습니다!</span>
                </div>
                <button onclick="submitInquiry()" id="submit-button" class="w-full bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white font-semibold py-3 px-6 rounded-lg shadow-md transition-all flex items-center justify-center">
                    <svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">
                        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>
                    </svg>
                    문의하기
                </button>
                <button onclick="goToPage('type')" class="w-full bg-gray-200 hover:bg-gray-300 text-gray-700 font-semibold py-3 px-6 rounded-lg shadow-md transition-all">
                    취소
                </button>
            </div>
        </div>

        <div class="text-center mt-6 text-gray-600 text-sm">
            <p>문의하신 내용은 실시간으로 관리자에게 전달됩니다</p>
            <p class="mt-1">빠른 시일 내에 답변드리겠습니다 😊</p>
        </div>
    </div>

    <script>
        var TELEGRAM_BOT_TOKEN = '8275814150:AAGiFsnueB7RaomovPkd_CXI63XhiQUkV9k';
        var TELEGRAM_CHAT_ID = '6192728624';

        var state = {
            selectedBranch: '',
            selectedBranchName: '',
            selectedType: '',
            selectedTypeName: '',
            selectedTypeIcon: ''
        };

        var inquiryTypes = [
            { id: 'room', title: '스터디룸 예약', icon: '📅' },
            { id: 'report', title: '학습 방해 행위 신고', icon: '🚨' },
            { id: 'parking', title: '주차 문의', icon: '🚗', excludeBranches: ['bupyeong'] },
            { id: 'parking_info', title: '주차 안내', icon: '🅿️', onlyBranches: ['bupyeong'], isInfo: true },
            { id: 'temperature', title: '온도 조절 문의', icon: '🌡️' },
            { id: 'other', title: '그 외 기타 문의', icon: '💬' }
        ];

        function goToPage(page) {
            document.getElementById('page-branch').classList.add('hidden');
            document.getElementById('page-type').classList.add('hidden');
            document.getElementById('page-form').classList.add('hidden');
            document.getElementById('page-parking-info').classList.add('hidden');
            
            if (page === 'branch') {
                document.getElementById('page-branch').classList.remove('hidden');
                state.selectedBranch = '';
                state.selectedBranchName = '';
                state.selectedType = '';
                state.selectedTypeName = '';
                state.selectedTypeIcon = '';
            } else if (page === 'type') {
                document.getElementById('page-type').classList.remove('hidden');
                document.getElementById('seat-number').value = '';
                document.getElementById('inquiry-content').value = '';
                document.getElementById('error-message').classList.add('hidden');
                document.getElementById('success-message').classList.add('hidden');
            } else if (page === 'form') {
                document.getElementById('page-form').classList.remove('hidden');
            } else if (page === 'parking-info') {
                document.getElementById('page-parking-info').classList.remove('hidden');
            }
        }

        function selectBranch(id, name, icon) {
            state.selectedBranch = id;
            state.selectedBranchName = name;
            document.getElementById('selected-branch-name').textContent = name;
            
            var typesContainer = document.getElementById('inquiry-types');
            typesContainer.innerHTML = '';
            
            for (var i = 0; i < inquiryTypes.length; i++) {
                var type = inquiryTypes[i];
                
                // 제외할 지점 체크
                if (type.excludeBranches && type.excludeBranches.indexOf(id) !== -1) {
                    continue;
                }
                
                // 특정 지점만 표시
                if (type.onlyBranches && type.onlyBranches.indexOf(id) === -1) {
                    continue;
                }
                
                var button = document.createElement('button');
                button.className = 'w-full p-4 bg-gradient-to-r from-indigo-500 to-purple-500 hover:from-indigo-600 hover:to-purple-600 text-white rounded-xl shadow-md transition-all transform hover:scale-105 flex items-center justify-between';
                button.innerHTML = '<span class="text-lg font-medium">' + type.title + '</span><span class="text-2xl">' + type.icon + '</span>';
                
                if (type.isInfo) {
                    button.onclick = function() {
                        goToPage('parking-info');
                    };
                } else {
                    button.onclick = (function(typeId, typeTitle, typeIcon) {
                        return function() {
                            selectType(typeId, typeTitle, typeIcon);
                        };
                    })(type.id, type.title, type.icon);
                }
                
                typesContainer.appendChild(button);
            }
            
            goToPage('type');
        }

        function selectType(id, title, icon) {
            state.selectedType = id;
            state.selectedTypeName = title;
            state.selectedTypeIcon = icon;
            
            document.getElementById('form-branch-name').textContent = state.selectedBranchName;
            document.getElementById('form-type-name').textContent = title;
            document.getElementById('form-type-icon').textContent = icon;
            document.getElementById('form-type-title').textContent = title;
            
            goToPage('form');
        }

        function submitInquiry() {
            var seatNumber = document.getElementById('seat-number').value;
            var inquiryContent = document.getElementById('inquiry-content').value;
            
            if (!seatNumber || !inquiryContent) {
                document.getElementById('error-message').classList.remove('hidden');
                return;
            }
            
            document.getElementById('error-message').classList.add('hidden');
            document.getElementById('success-message').classList.add('hidden');
            
            var submitButton = document.getElementById('submit-button');
            submitButton.disabled = true;
            submitButton.innerHTML = '전송 중...';
            
            var message = '🏢 에브라임 스터디카페 문의\n\n';
            message = message + '📍 지점: ' + state.selectedBranchName + '\n';
            message = message + '📋 문의 유형: ' + state.selectedTypeIcon + ' ' + state.selectedTypeName + '\n';
            message = message + '💺 좌석 번호: ' + seatNumber + '번\n';
            message = message + '📝 문의 내용:\n' + inquiryContent + '\n\n';
            message = message + '⏰ 접수 시간: ' + new Date().toLocaleString('ko-KR');
            
            var url = 'https://api.telegram.org/bot' + TELEGRAM_BOT_TOKEN + '/sendMessage';
            var data = {
                chat_id: TELEGRAM_CHAT_ID,
                text: message
            };
            
            fetch(url, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(data)
            })
            .then(function(response) {
                var iconSvg = '<svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">';
                iconSvg = iconSvg + '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>';
                iconSvg = iconSvg + '</svg>';
                
                submitButton.disabled = false;
                submitButton.innerHTML = iconSvg + '문의하기';
                
                if (response.ok) {
                    document.getElementById('success-message').classList.remove('hidden');
                    setTimeout(function() {
                        goToPage('branch');
                    }, 2000);
                } else {
                    document.getElementById('error-message').classList.remove('hidden');
                }
            })
            .catch(function(error) {
                var iconSvg = '<svg class="w-5 h-5 mr-2" fill="none" stroke="currentColor" viewBox="0 0 24 24">';
                iconSvg = iconSvg + '<path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 19l9 2-9-18-9 18 9-2zm0 0v-8"></path>';
                iconSvg = iconSvg + '</svg>';
                
                console.error('Error:', error);
                submitButton.disabled = false;
                submitButton.innerHTML = iconSvg + '문의하기';
                document.getElementById('error-message').classList.remove('hidden');
            });
        }
    </script>
</body>
</html>
