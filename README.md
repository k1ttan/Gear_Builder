Cấu hình cơ sở dữ liệu tại file application.properties:  
spring.datasource.url=jdbc:mysql://localhost:3306/gearbuilderdb #Tạo 1 db trống như tên  
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver #Cấu hình driver kết nối db  
spring.datasource.username=root #Username của db  
spring.datasource.password= #Password  

Sau đó chạy Terminal project với lệnh: 
```
mvn clean install
```

Cấu hình chạy project SpringBoot với tool có sẵn trên IDE với tomcat server  
Project sẽ chạy trên url: http://localhost:8080/

Thực hiện lệnh sql để có dữ liệu trong db:
```
INSERT INTO `product` (`id`, `category`, `description`, `discount`, `discount_price`, `image`, `is_active`, `price`, `stock`, `title`) VALUES
(1, 'CPU', 'Thông tin kỹ thuật CPU\r\nSố lõi: 6\r\nTổng số luồng: 12\r\nTần số turbo tối đa: 4.50 GHz\r\nBộ nhớ đệm: 12 MB Intel® Smart Cache\r\nBus Speed: 8 GT/s\r\nTần số TDP-up có thể cấu hình: 2.70 GHz\r\nTDP-up có thể cấu hình: 45 W\r\nTần số TDP-down có thể cấu hình: 2.20 GHz\r\nTDP-down có thể cấu hình: 35 W', 0, 2000000, 'danh-gia-hieu-nang-on-dinh-tren-intel-core-i5-11400h2.jpg', b'1', 2000000, 3, 'Core I5-11400H'),
(2, 'CPU', 'abc', 0, 2000000, 'intel-core-i5-12400f_e62f0661a4ce498cb23a585cafbe460a_master.webp', b'1', 2000000, 5, 'Core I5-12400F'),
(3, 'CPU', '', 0, 2000000, 'images.jpg', b'1', 2000000, 5, 'Core I5-13400F'),
(5, 'CPU', 'avc', 0, 2000000, 'images.jpg', b'1', 2000000, 5, 'Core I5-13400F'),
(6, 'Nguồn', '750W, 80 Plus Gold, Full Modular, Quạt 120mm Zero RPM', 0, 2450000, 'corsair_rm750x.jpg', b'1', 2450000, 15, 'Corsair RM750x (2021)'),
(7, 'Nguồn', '850W, 80 Plus Gold, Full Modular, ECO Mode', 0, 3200000, 'evga_g6_850.jpg', b'1', 3200000, 8, 'EVGA SuperNOVA 850 G6'),
(8, '--select--', '550W, 80 Plus Platinum, Full Modular, 10 năm bảo hành', 0, 2100000, 'seasonic_px550.jpg', b'1', 2100000, 12, 'Seasonic FOCUS PX-550'),
(9, 'Nguồn', '850W, 80 Plus Gold, SFX Form Factor, Modular', 0, 3500000, 'cm_v850_sfx.jpg', b'1', 3500000, 10, 'Cooler Master V850 SFX	'),
(10, 'Nguồn', '600W, 80 Plus Gold, Bán Modular, Silent Wings 3', 0, 3500000, 'bequiet_pp11.jpg', b'1', 3500000, 10, 'Pure Power 11 600W'),
(11, 'Nguồn', '	1000W, 80 Plus Gold, ATX 3.0, PCIe Gen 5.0', 0, 4300000, 'tt_gf3_1000w.jpg', b'1', 4300000, 0, 'Thermaltake Toughpower GF3'),
(12, 'Ổ cứng', 'SSD M.2 NVMe 500GB, Đọc 3500MB/s, Ghi 3000MB/s, PCIe Gen3x4', 10, 1071000, 'Samsung 970 EVO Plus 500GB.png', b'1', 1190000, 15, 'Samsung 970 EVO Plus 500GB'),
(13, 'Ổ cứng', 'HDD 3.5\" 2TB, 7200RPM, SATA III, 256MB Cache', 0, 1059000, 'Seagate BarraCuda 2TB.png', b'1', 1059000, 20, 'Seagate BarraCuda 2TB'),
(14, 'Ổ cứng', 'SSD M.2 NVMe 1TB, Đọc 2400MB/s, Ghi 1950MB/s, PCIe Gen3', 15, 1785000, 'WD Blue SN570 1TB.png', b'1', 2100000, 12, 'WD Blue SN570 1TB'),
(15, 'Ổ cứng', 'SSD 2.5\" SATA 1TB, Đọc 560MB/s, Ghi 510MB/s, 3D NAND', 5, 1852500, 'Crucial MX500 1TB.png', b'1', 1950000, 8, 'Crucial MX500 1TB'),
(16, 'Ổ cứng', 'HDD 3.5\" 4TB, 7200RPM, SATA III, 256MB Cache, Hiệu suất cao', 0, 2890000, 'WD Black 4TB.png', b'0', 2890000, 0, 'WD Black 4TB'),
(17, 'Ổ cứng', 'SSD M.2 NVMe 2TB, Đọc 7000MB/s, Ghi 5300MB/s, PCIe Gen4', 20, 3992000, 'Samsung 980 Pro 2TB.png', b'1', 4990000, 5, 'Samsung 980 Pro 2TB'),
(18, 'Ổ cứng', 'SSD Portable 1TB, USB 3.2 Gen 2, Chống sốc, IP65', 10, 1791000, 'SanDisk Extreme Portable 1TB.png', b'1', 1990000, 18, 'SanDisk Extreme Portable 1TB'),
(19, 'Ổ cứng', 'HDD 3.5\" 8TB, 7200RPM, SATA III, 256MB Cache, NAS', 0, 4590000, 'Toshiba N300 8TB.png', b'1', 4590000, 6, 'Toshiba N300 8TB'),
(20, 'Ổ cứng', 'SSD M.2 NVMe 1TB, Đọc 5000MB/s, Ghi 4400MB/s, PCIe Gen4', 12, 3062400, 'Kingston Fury Renegade 1TB.png', b'1', 3480000, 9, 'Kingston Fury Renegade 1TB'),
(21, 'Ổ cứng', 'SSD External 2TB, USB-C 3.2, Chống nước, Bảo mật phần mềm', 25, 2992500, 'Samsung T7 Shield 2TB.png', b'1', 3990000, 11, 'Samsung T7 Shield 2TB'),
(22, 'GPU', 'GeForce RTX 4090, 24GB GDDR6X, 384-bit, DLSS 3, Ada Lovelace', 0, 51990000, 'ASUS ROG Strix GeForce RTX 4090.png', b'1', 51990000, 4, 'ASUS ROG Strix GeForce RTX 4090'),
(23, 'GPU', 'Radeon RX 7900 XTX, 24GB GDDR6, 384-bit, Raytracing, FSR 3', 8, 23864800, 'Sapphire Nitro+ RX 7900 XTX.png', b'1', 25940000, 7, 'Sapphire Nitro+ RX 7900 XTX'),
(24, 'GPU', 'GeForce RTX 4080, 16GB GDDR6X, 256-bit, DLSS 3, 4K Gaming', 12, 33088000, 'MSI Gaming X Trio RTX 4080.png', b'1', 37600000, 5, 'MSI Gaming X Trio RTX 4080'),
(25, 'GPU', 'Radeon RX 7800 XT, 16GB GDDR6, 256-bit, Infinity Cache, AV1', 0, 12990000, 'XFX Speedster RX 7800 XT.png', b'1', 12990000, 9, 'XFX Speedster RX 7800 XT'),
(26, 'GPU', 'GeForce RTX 4070, 12GB GDDR6X, 192-bit, DLSS 3, 1440p Ultra', 10, 17010000, 'Gigabyte Gaming OC RTX 4070.png', b'1', 18900000, 11, 'Gigabyte Gaming OC RTX 4070'),
(27, 'GPU', 'Radeon RX 7600, 8GB GDDR6, 128-bit, 1080p Gaming, Low Power', 15, 6783000, 'ASRock Challenger RX 7600.png', b'1', 7980000, 15, 'ASRock Challenger RX 7600'),
(28, 'GPU', 'GeForce RTX 4060 Ti, 8GB GDDR6, 128-bit, DLSS 3, AV1 Encode', 20, 8800000, 'Zotac Twin Edge RTX 4060 Ti.png', b'0', 11000000, 0, 'Zotac Twin Edge RTX 4060 Ti'),
(29, 'GPU', 'Radeon RX 6750 XT, 12GB GDDR6, 192-bit, 1440p Performance', 20, 7992000, 'powercolor_hellhound_6750xt.jpg', b'1', 9990000, 6, 'PowerColor Hellhound RX 6750 XT'),
(30, 'GPU', 'GeForce RTX 3060, 12GB GDDR6, 192-bit, Raytracing, DLSS', 25, 5992500, 'pny_verto_rtx3060.jpg', b'1', 7990000, 8, 'PNY Verto RTX 3060 12GB'),
(31, 'GPU', 'Radeon RX 6600, 8GB GDDR6, 128-bit, 1080p Gaming, Cooler', 0, 5490000, 'msi_mech_rx6600.jpg', b'1', 5490000, 12, 'MSI Mech RX 6600'),
(32, 'RAM', '32GB (2x16GB) DDR5 6000MHz, CL30, XMP 3.0, RGB Lighting', 15, 3825000, 'corsair_vengeance_rgb.jpg', b'1', 4500000, 12, 'Corsair Vengeance RGB DDR5 32GB'),
(33, 'RAM', '32GB (2x16GB) DDR4 3600MHz, CL16, Trident Z Neo, AMD Optimized', 10, 3591000, 'gskill_trident_z.jpg', b'1', 3990000, 8, 'G.Skill Trident Z Neo DDR4 32GB'),
(34, 'RAM', '16GB (1x16GB) DDR5 4800MHz, CL40, Plug and Play, Low Profile', 0, 1150000, 'kingston_fury_beast.jpg', b'1', 1150000, 25, 'Kingston Fury Beast DDR5 16GB'),
(35, 'RAM', '64GB (2x32GB) DDR5 5600MHz, CL40, XMP 3.0, Aluminum Heatspreader', 20, 5592000, 'crucial_pro_ram.jpg', b'1', 6990000, 4, 'Crucial Pro DDR5 64GB'),
(36, 'RAM', '16GB (2x8GB) DDR4 3200MHz, CL16, T-Force Delta RGB, ARGB Sync', 25, 1492500, 'teamgroup_delta_rgb.jpg', b'1', 1990000, 15, 'TeamGroup T-Force Delta RGB 16GB'),
(37, 'RAM', '128GB (4x32GB) DDR5 5200MHz, CL38, ECC Registered, Server Grade', 0, 12990000, 'samsung_ecc_ram.jpg', b'0', 12990000, 0, 'Samsung DDR5 ECC 128GB'),
(38, 'RAM', '32GB (2x16GB) DDR4 3200MHz, CL22, Laptop SODIMM, 1.2V', 5, 1900000, 'sk_hynix_laptop.jpg', b'1', 2000000, 18, 'SK Hynix DDR4 Laptop 32GB'),
(39, 'RAM', '64GB (2x32GB) DDR4 3600MHz, CL18, Dominator Platinum, RGB', 12, 7040000, 'corsair_dominator.jpg', b'1', 8000000, 6, 'Corsair Dominator Platinum DDR4 64GB'),
(40, 'RAM', '8GB (1x8GB) DDR3 1600MHz, CL11, Desktop Memory, Value Series', 30, 420000, 'adata_ddr3.jpg', b'1', 600000, 30, 'ADATA Premier DDR3 8GB'),
(41, 'RAM', '32GB (2x16GB) DDR5 7200MHz, CL34, XMP 3.0, Intel XMP Certified', 8, 6440000, 'gskill_trident_z5.jpg', b'1', 7000000, 3, 'G.Skill Trident Z5 RGB DDR5 32GB'),
(42, 'PC Build sẵn', 'CPU: Intel Core i5-13400F, GPU: RTX 4060 Ti 8GB, RAM: 16GB DDR4 3200MHz, Ổ cứng: SSD 1TB NVMe, Nguồn: 650W 80 Plus Bronze. PC gaming 1080p Ultra, tản nhiệt khí hiệu quả, vỏ Mid-tower RGB', 10, 22950000, 'skytech_gaming_pc.jpg', b'1', 25500000, 7, 'SkyTech Gaming PC - RTX 4060 Ti'),
(43, 'PC Build sẵn', 'CPU: AMD Ryzen 7 7700X, GPU: RX 7800 XT 16GB, RAM: 32GB DDR5 5600MHz, Ổ cứng: SSD 2TB PCIe 4.0, Nguồn: 750W Gold. Workstation đa nhiệm + gaming 1440p, vỏ NZXT H5 Flow, tản nước AIO 240mm', 0, 37990000, 'origin_pc_workstation.jpg', b'1', 37990000, 4, 'Origin PC Creator Workstation'),
(44, 'PC Build sẵn', 'CPU: Intel Core i9-14900K, GPU: RTX 4090 24GB, RAM: 64GB DDR5 6000MHz, Ổ cứng: 2TB NVMe + 4TB HDD, Nguồn: 1000W Platinum. Máy trạm 8K/VR, vỏ Lian Li O11 Dynamic, tản nước custom, 10 fan RGB', 5, 75990000, 'digital_storm_elite.jpg', b'1', 79990000, 2, 'Digital Storm Apex Elite'),
(45, 'PC Build sẵn', 'CPU: AMD Ryzen 5 5600G, GPU: Radeon Graphics (APU), RAM: 16GB DDR4 3200MHz, Ổ cứng: SSD 512GB, Nguồn: 500W 80 Plus. PC văn phòng tối giản, vỏ SFF mini-ITX, không cần card rời, chạy mát và êm', 15, 10965000, 'hp_slim_desktop.jpg', b'1', 12900000, 12, 'HP Slim Desktop Office Pro'),
(46, 'PC Build sẵn', 'CPU: Intel Core i7-13700KF, GPU: RTX 4070 Super 12GB, RAM: 32GB DDR5 5200MHz, Ổ cứng: 1TB NVMe + 2TB HDD, Nguồn: 850W Gold. Build màu trắng toàn bộ, 6 fan ARGB, tản nhiệt DeepCool AK620', 12, 35200000, 'nzxt_white_build.jpg', b'1', 40000000, 5, 'NZXT H9 Flow White Edition'),
(47, 'PC Build sẵn', 'CPU: AMD Ryzen 9 7950X3D, GPU: RX 7900 XTX 24GB, RAM: 64GB DDR5 6000MHz, Ổ cứng: 4TB NVMe RAID 0, Nguồn: 1200W Titanium. Cấu hình đỉnh cho streamer, render 3D, benchmark, vỏ Hyte Y60 kính cường lực', 8, 65992000, 'maingear_ultimate.jpg', b'0', 71730000, 0, 'Maingear F131 Ultimate'),
(48, 'PC Build sẵn', 'CPU: Intel Core i3-12100F, GPU: GTX 1650 4GB, RAM: 8GB DDR4 2666MHz, Ổ cứng: 256GB SSD + 1TB HDD, Nguồn: 450W Bronze. PC giá rẻ cho học tập, vỏ Micro-ATX đơn giản, không RGB', 20, 9992000, 'dell_budget_pc.jpg', b'1', 12490000, 15, 'Dell Inspiron Gaming Desktop'),
(49, 'PC Build sẵn', 'CPU: Apple M2 Max, GPU: 38-core GPU, RAM: 64GB Unified, Ổ cứng: 4TB SSD, Nguồn: Integrated. Mac Studio cho sáng tạo chuyên nghiệp, hỗ trợ 8K video, thiết kế nhôm nguyên khối', 0, 87990000, 'mac_studio.jpg', b'1', 87990000, 1, 'Apple Mac Studio M2 Max'),
(50, 'PC Build sẵn', 'CPU: AMD Ryzen 7 5800X3D, GPU: RTX 3080 10GB, RAM: 32GB DDR4 3600MHz, Ổ cứng: 2TB NVMe, Nguồn: 850W Gold. Build chuyên game Esports (Valorant/CS2), độ trễ thấp, màn hình 360Hz-ready', 18, 31160000, 'cyberpower_esports.jpg', b'1', 38000000, 5, 'CyberPowerPC Esports Ready');

```
