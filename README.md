<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ร้านย่างหมึก - ช่องทางการติดต่อ</title>
    <!-- โหลด Tailwind CSS CDN --><script src="https://cdn.tailwindcss.com"></script>
    <!-- โหลด Font Awesome สำหรับไอคอน --><link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0-beta3/css/all.min.css">
    
    <!-- เพิ่ม: ลิงก์ Google Font สำหรับ Kanit (Kanit Font Link) --><link href="https://fonts.googleapis.com/css2?family=Kanit:wght@400;600;700&display=swap" rel="stylesheet">

    <style>
        /* กำหนดค่าเริ่มต้นสำหรับ Tailwind */
        :root {
            --color-primary: #dc2626; /* สีแดงสำหรับร้านย่าง (Grilled/Chili Red) */
        }
        
        /* อัปเดต: ใช้ฟอนต์ Kanit เป็นหลัก */
        body {
            font-family: 'Kanit', sans-serif;
            background-color: #fef3c7; /* สีเหลืองอ่อนๆ คล้ายกระดาษห่ออาหาร/แสงไฟ */
        }
        
        /* อัปเดต: เงาสำหรับปุ่ม (เพิ่ม shadow-md) */
        .contact-button {
            transition: all 0.2s;
            box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1); /* เพิ่มเงาเริ่มต้น */
        }

        .contact-button:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 10px rgba(0, 0, 0, 0.15); /* เงาเข้มขึ้นเมื่อโฮเวอร์ */
        }
        
        /* สีกำหนดเองสำหรับปุ่มโซเชียลมีเดีย */
        .facebook-bg { background-color: #1877F2; }
        .line-bg { background-color: #00B900; }
        .tiktok-bg { background-color: #000000; }
        
        /* CSS สำหรับ Preloader */
        #preloader {
            transition: opacity 0.5s ease-out; /* สำหรับการทำ Fade out */
        }
    </style>

    <script>
        tailwind.config = {
            theme: {
                extend: {
                    colors: {
                        primary: 'var(--color-primary)',
                    }
                }
            }
        }
    </script>
</head>
<body class="flex items-center justify-center min-h-screen p-4">

    <!-- Preloader (หน้าจอโหลด) --><div id="preloader" class="fixed inset-0 flex flex-col items-center justify-center bg-[#fef3c7] z-50">
        <!-- โลโก้คาแรคเตอร์สำหรับ Preloader (รูป ย่างหมึกเดินได้) --><img src="https://i.imgur.com/1Dz9aE5.png" alt="โลโก้ร้านย่างหมึกกำลังโหลด" class="w-48 h-auto max-w-[50vw]"
             onerror="this.onerror=null; this.src='https://placehold.co/192x192/fef3c7/dc2626?text=LOADING'"> 
        <p class="mt-4 text-xl font-bold text-primary animate-pulse">กำลังโหลด...</p>
    </div>

    <!-- Container หลัก --><div class="w-full max-w-sm bg-white p-8 rounded-xl shadow-2xl text-center">
        
        <!-- ส่วนโลโก้และชื่อร้าน --><div class="mb-8">
            <!-- โลโก้หลัก (รูปปลาหมึกย่าง) --><img src="https://i.imgur.com/c9aaJDt.jpeg"  alt="โลโก้ร้านย่างหมึก" 
                 class="w-32 h-32 object-cover mx-auto rounded-full border-4 border-primary shadow-lg"
                 onerror="this.onerror=null; this.src='https://placehold.co/128x128/dc2626/ffffff?text=Y+M'">
            
            <h1 class="text-3xl font-bold mt-4 text-gray-800">ร้านย่างหมึก</h1>
        </div>

        <!-- รายการปุ่มติดต่อ --><div class="space-y-4">
            
            <!-- Facebook --><a href="https://www.facebook.com/share/1CpnYTozKr/?mibextid=wwXIfr" 
               target="_blank" 
               class="contact-button facebook-bg text-white w-full flex items-center justify-center py-3 rounded-xl font-medium text-lg uppercase shadow-md"> 
                <i class="fab fa-facebook-f mr-3 text-xl"></i>
                Facebook Page
            </a>

            <!-- Line --><a href="https://line.me/R/ti/p/@622yuaej" 
               target="_blank" 
               class="contact-button line-bg text-white w-full flex items-center justify-center py-3 rounded-xl font-medium text-lg uppercase shadow-md"> 
                <i class="fab fa-line mr-3 text-xl"></i>
                Line Official
            </a>

            <!-- TikTok --><a href="https://www.tiktok.com/@yangmuek?_r=1&_t=ZS-91LUebe3aRp" 
               target="_blank" 
               class="contact-button tiktok-bg text-white w-full flex items-center justify-center py-3 rounded-xl font-medium text-lg uppercase shadow-md"> 
                <i class="fab fa-tiktok mr-3 text-xl"></i>
                TikTok
            </a>
            
        </div>
        
        <p class="mt-8 text-sm text-gray-500">
            <!-- ข้อความเล็กๆ ท้ายหน้า -->คลิกที่ช่องทางด้านบนเพื่อสอบถามรายละเอียดเพิ่มเติม
        </p>

    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {
            const preloader = document.getElementById('preloader');
            
            // ซ่อน Preloader เมื่อเนื้อหาทั้งหมดโหลดเสร็จ
            window.onload = function() {
                // ทำให้ Preloader ค่อยๆ หายไป
                preloader.style.opacity = '0';
                
                // ซ่อน Preloader หลังจากจบ Transition เพื่อให้ไม่บังการคลิก
                setTimeout(() => {
                    preloader.style.display = 'none';
                }, 500); // 500ms ตรงกับค่า transition ใน CSS
            };
        });
    </script>
</body>
</html>


