# 在Win 10 64bit上的Visual Studio中安裝及設定opencv 2.4.13
### 參考網站:
```
https://blogs.msdn.microsoft.com/microsoft_student_partners_in_taiwan/2016/05/14/%E5%B0%87opencv%E5%AE%8C%E7%BE%8E%E5%BB%BA%E7%BD%AE%E6%96%BCvisual-studio%E4%B8%8A/?fbclid=IwAR1uZyjI2HcAyQmWs1tOMklHU2SuLcDQGVN8zUj5OZRhchlDzgyxCpLgWa0
```
**安裝 opencv 2.4.13**
解壓縮 opencv-2.4.13.3-vc14.exe

**設定環境變數**

本機(點右鍵) → 內容 → 進階系統設定 → 環境變數 → path → 編輯 新增以下資料：
```
C:\opencv\build\x64\vc14\bin;
```

**新增C++檔案**
開啟Visual Studio後，新增專案 → 左側「Visual C++」 → Win32 主控台應用程式→ 輸入專案名稱 → 確定 → 下一步 → 僅勾取「空專案」就好 → 完成 → 在資源檔新增C++檔案

**設定**
* 1.設定VC++目錄 → 在「Include目錄」增加 `C:\opencv\build\include`
* 2.設定VC++目錄 → 在「程式庫目錄」增加 `C:\opencv\build\x64\vc14\lib`
* 3.C/C++ → 一般(general) → include 目錄 中include 以下三個資料夾的位置：
    
    略.../build/include/
    
    略.../build/include/opencv/
    
    略.../build/include/opencv2
* 4.連結器 → 一般 → 其他程式庫目錄 中新增：
```
opencv_calib3d2413d.lib
opencv_contrib2413d.lib
opencv_core2413d.lib
opencv_features2d2413d.lib
opencv_flann2413d.lib
opencv_gpu2413d.lib
opencv_highgui2413d.lib
opencv_imgproc2413d.lib
opencv_legacy2413d.lib
opencv_ml2413d.lib
opencv_nonfree2413d.lib
opencv_objdetect2413d.lib
opencv_ocl2413d.lib
opencv_photo2413d.lib
opencv_stitching2413.lib
opencv_calib3d2413d.lib
opencv_contrib2413d.lib
opencv_core2413d.lib
opencv_features2d2413d.lib
opencv_flann2413d.lib
opencv_gpu2413d.lib
opencv_highgui2413d.lib
opencv_imgproc2413d.lib
opencv_legacy2413d.lib
opencv_ml2413d.lib
opencv_nonfree2413d.lib
opencv_objdetect2413d.lib
opencv_ocl2413d.lib
opencv_photo2413d.lib
opencv_stitching2413d.lib
opencv_superres2413d.lib
opencv_ts2413d.lib
opencv_video2413d.lib
opencv_videostab2413d.lib
opencv_stitching2413d.lib
opencv_superres2413d.lib
opencv_ts2413d.lib
opencv_video2413d.lib
opencv_videostab2413d.lib
```