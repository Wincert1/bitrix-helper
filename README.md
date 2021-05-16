<h3>CIBlockElement::GetList</h3>

    $rs = CIBlockElement::GetList(Array("NAME"=>"asc"), array("IBLOCK_ID"=>1), false, false, array("ID", "NAME", "PROPERTY_", "CATALOG_PRICE_1"));
    while ($ar = $rs->GetNext()) {
        p($ar);
    }

<h3>Мелочи</h3>

    CModule::IncludeModule("iblock");

<h1>Работа с разделами</h1>
Путь от корня разделов до текущего раздела:

    $rs = CIBlockSection::GetNavChain(1, $ar['IBLOCK_SECTION_ID']);
    if ($ar = $rs->GetNext()) {
        p($ar, false);
    }

<h3>Подключаем ядро</h3>

    require_once($_SERVER['DOCUMENT_ROOT'] . "/bitrix/modules/main/include/prolog_before.php");
