# HRC_ROBOT_2026

Thiết kế mạch PCB & Schematic cho xe dò line **HUST Robotic Competition 2026 (HRC 2026)** sử dụng **KiCad 10**.

## Tổng quan phần cứng
- **Vi điều khiển:** STM32F411CEU6 BlackPill
- **Driver động cơ:** TB6612FNG (hỗ trợ 2 động cơ N20 kèm encoder)
- **Nguồn:** Pin LiPo 2S (7.4V) qua XT30 (`J_BAT`), hạ áp 5V qua module Buck MP1584EN (`MP1`)
- **Cảm biến dò line:** Mảng 8+1 mắt hồng ngoại TCRT5000 bố trí cong (Kiểu 3) nối với bo chính qua cáp 12 chân (`J_IR` ↔ `J_IR_BOARD`)
- **Cảm biến bổ trợ:** IMU MPU6050 (`J_MPU` - I2C), cảm biến khoảng cách VL53L0X (`J_TOF` - I2C + XSHUT), cổng debug `UART`

## Các file chính để kiểm tra
- **KiCad Project:** `My_PCB.kicad_pro`
- **Schematic:** `My_PCB.kicad_sch` và trang con `TCRT_sensors.kicad_sch`
- **PCB (đã đi dây 2 lớp & phủ đồng GND chuẩn JLCPCB):** `My_PCB.kicad_pcb`
- **PCB (bản chỉ xếp linh kiện chưa đi dây):** `My_PCB_unrouted_pro.kicad_pcb`
- **Thư viện footprint riêng:** `customs.pretty/` và `fp-lib-table`
- **Bản xem nhanh PDF:** `schematic_perfect.pdf` và `pcb_routed_final.pdf`
