#Sanctum manage
- กำหนดวันหมดอายุของ Token (ปกติ token ของ sanctum จะไม่มีวันหมดอายุ) 
    - 'expiration' => 43800, // 30 days  : ใน file config/sanctum.php
- กำหนดให้ลบ token sanctum ที่หมดอายุ
    - $schedule->command('sanctum:prune-expired --hours=24')->daily(); // จะลบโทเค็นที่หมดอายุหลังจาก 24ชม ทุกๆวัน
    - กำหนดใน function schedule() : ใน file app/Console/Kernel.php
