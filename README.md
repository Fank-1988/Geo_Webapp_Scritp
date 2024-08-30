# Geo_Webapp_Scritp

กิจกรรม doGet ( e ) {
ส่งความถี่HtmlService createTemplateFromFile ( "ดัชนี" ) . ประเมิน( )
ข้อมูล ผู้ใช้Click ( ข้อมูล) {
ให้ ss = SpreadsheetApp ​openById ( 'xxx' ) ;
ให้ งาน= ss รับชีต ( ) [ 0 ] ;
ให้ ตอบ กลับ= Maps แทน Geocoder ( ) . ReverseGeocode ( data.lat , data.lon ) ;
ให้ geoAddress = การตอบสนองผลลัพธ์[ 0 ] . จัดรูปแบบ_ที่อยู่;
งานappendRow ( [ data .username , Utilities . formatDate ( new Date ( ) , "GMT+7" , "MM/dd/yyyy HH :mm:ss" ) , $ { data .lat } , $ { data . lon } , ทางคืนนี้] )

#
var strYear543 = parseInt ( Utilities . formatDate ( วันที่เดท ( ) , "Asia/Bangkok" , "yyyy" ) ) + 543 ;
var strhour = ยูทิลิตี้formatDate ( วันที่เดท ( ) , "เอเชีย/กรุงเทพฯ" , "HH" ) ;
var strMinute = ยูทิลิตี้formatDate ( วันที่เดท ( ) , "เอเชีย/กรุงเทพฯ" , "mm" ) ;
var strMonth1 = ยูทิลิตี้formatDate ( วันที่อัพเดต ( ) , "เอเชีย/กรุงเทพฯ" , "M" ) ;
var strMonthCut1 = [ "" , "มกราคม" , "กุมภาพันธ์" , "มีนาคม" , " เมษายน" , "อาจ" , "มิถุนายนายนายน" , "กรกฎาคม" , "สิงหาคม" , "ยายกันน" , " กล่าวถึง " , "พฤศจิกายน" , "ธันวาคม" ]
var strMonthThai = strMonthCut1 [ strMonth1 ] ;
var strDay = ยูทิลิตี้formatDate ( วันที่เดท ( ) , "เอเชีย/กรุงเทพฯ" , "d" ) ; // d ไม่มี 0 นำ dd มี 0 นำ
var กลางวัน= strDay + ' ' + strMonthThai + ' ' + strYear543 + ' เวลา ' + strhour + ':' + strMinute + ' น.' -

#
var text_data1 = '📣 แจ้งพิกัดการเช็คอิน\n' ;
text_data1 += '⏰วัน-เวลา\n' + ' \ n👨‍💼 ชื่อ- นามสกุล\n' + data บันทึก+ '\n📌 Location\n' + ข้อมูล. ละติจูด+ "," + ข้อมูล. lon + '\n หอพัก\n' + geoAddress
#
ละติจูด var = ข้อมูล​ละติจูด
ลองจิจูด var = ข้อมูล​โหลน
var map = แผนที่​ใหม่ StaticMap ( )
#
setSize ( 600 , 600 ) //(สูงสุด:1300 X 1300
-  ตั้งค่าภาษา( 'TH' )
-  setMobile ( จริง)
-  setMapType ( แผนที่. ประเภทStaticMap . HYBRID )
#
เมพ. addMarker ( ละติจูด, ลองจิจูด)
var mapBlob = แผนที่​รับหยด( )
var mapUrl = แผนที่​รับ MapUrl ( )
ส่งHttpPostImage ( text_data1 , mapBlob )

#
วัน sendHttpPostImage ( mapUrl , mapBlob ) {
หลังจากนั้น var = "xxx" ;
var formData = {
'ข้อความ' : '\n' + mapUrl ,
'imageFile' : mapBlob
มี var =
"วิธีการ" : "โพสต์" ,
"เพย์โหลด" : formData , // วัฒนธรรม, รับรองภาพ, formData, ผู้ถือ
"ความเชื่อ" : { "การยึด" : " เป็นพิเศษ" + ความเชื่อ}
} ;


UrlFetchApp ​ดึงข้อมูล( "https://notify-api.line.me/api/notify" , รับชม) ;
