<h3>Мелочи</h3>

CModule::IncludeModule("iblock");


<h3>CIBlockElement::GetList</h3>

$rs = CIBlockElement::GetList(Array("NAME"=>"asc"), array("IBLOCK_ID"=>1), false, false, array("ID", "NAME"));
while ($ar = $rs->GetNext()) {
    p($ar);
}
