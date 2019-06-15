# Examples

`CATEGORIES:  
Going(I): yes; no  
MyCombo(AO): #selected {8 AM; 9 AM; 10 AM; 11 AM; 12 AM}; 10:30 AM; 7:59 AM; #label Select time; #available; error {invalid time; non-available time}; #selected; #typed “${BwdDEL}N”  
  
CONSTRAINTS:  
CheckError1:  
WHEN Going IS no  
  THEN MyCombo IS NOT #available   
WHEN Going IS yes  
  THEN MyCombo IS #available   
WHEN MyCombo IS 7:59 AM  
  THEN IT HAS error non-available time  
  
CheckError2:  
WHEN MyCombo IS 10:30 AM AND IT IS #typed “${BwdDEL}N”  
  THEN MyCombo HAS error invalid time   
  
Happy path list:  
WHEN MyCombo HAS #label Select time and IT IS 9 AM #selected  
  THEN …   
   
WHEN MyCombo HAS #label Select time and IT IS 9 AM THEN …   
  
Happy path select:  
WHEN MyCombo IS 10:30 AM  
  THEN …`

