<template>
  <div>
    <div id="stars2"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style lang="scss">
@import "../assets/_global.scss";

// html {
//   background: white;
// }

#stars2 {
  z-index: -10;
  width: 3px;
  height: 3px;
  // background: transparent;
  box-shadow: 1907px 1575px $starcolor, 893px 268px $starcolor,
    1819px 666px $starcolor, 366px 1985px $starcolor, 1736px 1062px $starcolor,
    1124px 45px $starcolor, 905px 1674px $starcolor, 1570px 711px $starcolor,
    255px 1747px $starcolor, 147px 1032px $starcolor, 865px 1813px $starcolor,
    1721px 1461px $starcolor, 202px 724px $starcolor, 1860px 812px $starcolor,
    634px 1410px $starcolor, 927px 1264px $starcolor, 1648px 620px $starcolor,
    1915px 1309px $starcolor, 731px 778px $starcolor, 91px 1185px $starcolor,
    829px 1003px $starcolor, 174px 1784px $starcolor, 1094px 1874px $starcolor,
    1464px 484px $starcolor, 1639px 1717px $starcolor, 959px 573px $starcolor,
    1686px 1287px $starcolor, 906px 356px $starcolor, 970px 499px $starcolor,
    626px 890px $starcolor, 1344px 1070px $starcolor, 1351px 544px $starcolor,
    708px 68px $starcolor, 1870px 130px $starcolor, 556px 1270px $starcolor,
    1432px 618px $starcolor, 769px 673px $starcolor, 1289px 1410px $starcolor,
    1499px 1969px $starcolor, 749px 1163px $starcolor, 1198px 198px $starcolor,
    399px 133px $starcolor, 1856px 1280px $starcolor, 904px 194px $starcolor,
    973px 1107px $starcolor, 1371px 1785px $starcolor, 989px 1835px $starcolor,
    1043px 1517px $starcolor, 787px 916px $starcolor, 1635px 1155px $starcolor,
    752px 524px $starcolor, 1926px 1279px $starcolor, 1052px 1163px $starcolor,
    719px 1963px $starcolor, 786px 519px $starcolor, 1440px 500px $starcolor,
    156px 1265px $starcolor, 1691px 429px $starcolor, 1349px 1474px $starcolor,
    736px 459px $starcolor, 248px 1678px $starcolor, 1136px 510px $starcolor,
    1317px 10px $starcolor, 1209px 1323px $starcolor, 54px 469px $starcolor,
    730px 1939px $starcolor, 960px 23px $starcolor, 112px 941px $starcolor,
    1852px 1522px $starcolor, 1993px 1972px $starcolor, 265px 129px $starcolor,
    222px 1897px $starcolor, 1766px 1804px $starcolor, 1530px 1786px $starcolor,
    1045px 432px $starcolor, 1916px 1980px $starcolor, 309px 1780px $starcolor,
    1420px 559px $starcolor, 1708px 103px $starcolor, 324px 1407px $starcolor,
    1175px 943px $starcolor, 80px 1221px $starcolor, 1016px 1933px $starcolor,
    318px 560px $starcolor, 190px 1489px $starcolor, 1095px 892px $starcolor,
    1975px 1191px $starcolor, 1197px 955px $starcolor, 1482px 873px $starcolor,
    1912px 300px $starcolor, 2000px 1636px $starcolor, 1473px 1808px $starcolor,
    507px 192px $starcolor, 924px 1300px $starcolor, 1485px 1636px $starcolor,
    41px 1822px $starcolor, 689px 120px $starcolor, 769px 273px $starcolor,
    1039px 976px $starcolor, 1057px 1520px $starcolor, 1417px 1187px $starcolor,
    512px 1507px $starcolor, 519px 45px $starcolor, 1207px 1687px $starcolor,
    1824px 1488px $starcolor, 1694px 31px $starcolor, 1859px 52px $starcolor,
    1368px 268px $starcolor, 190px 1404px $starcolor, 940px 1003px $starcolor,
    167px 942px $starcolor, 1641px 647px $starcolor, 1051px 654px $starcolor,
    233px 1640px $starcolor, 554px 511px $starcolor, 1705px 1866px $starcolor,
    240px 1430px $starcolor, 140px 668px $starcolor, 648px 1617px $starcolor,
    252px 101px $starcolor, 676px 1774px $starcolor, 889px 1698px $starcolor,
    595px 853px $starcolor, 249px 1768px $starcolor, 1091px 1529px $starcolor,
    223px 839px $starcolor, 239px 699px $starcolor, 1547px 356px $starcolor,
    249px 1130px $starcolor, 1209px 1946px $starcolor, 1967px 1274px $starcolor,
    430px 298px $starcolor, 1305px 134px $starcolor, 156px 91px $starcolor,
    1712px 264px $starcolor, 1256px 991px $starcolor, 1887px 1844px $starcolor,
    1957px 1275px $starcolor, 1718px 666px $starcolor, 1090px 543px $starcolor,
    933px 1411px $starcolor, 801px 323px $starcolor, 202px 1659px $starcolor,
    1117px 549px $starcolor, 290px 1859px $starcolor, 1380px 1516px $starcolor,
    557px 1165px $starcolor, 1953px 1758px $starcolor, 1901px 1407px $starcolor,
    1144px 347px $starcolor, 1640px 271px $starcolor, 1996px 43px $starcolor,
    838px 488px $starcolor, 1151px 1529px $starcolor, 306px 460px $starcolor,
    1666px 635px $starcolor, 1572px 633px $starcolor, 1797px 1076px $starcolor,
    1727px 1119px $starcolor, 474px 871px $starcolor, 1491px 1398px $starcolor,
    1301px 868px $starcolor, 1632px 454px $starcolor, 1611px 466px $starcolor,
    498px 1162px $starcolor, 796px 269px $starcolor, 1988px 747px $starcolor,
    502px 12px $starcolor, 276px 1260px $starcolor, 1536px 974px $starcolor,
    956px 656px $starcolor, 107px 701px $starcolor, 965px 491px $starcolor,
    1646px 247px $starcolor, 1515px 921px $starcolor, 1813px 519px $starcolor,
    697px 143px $starcolor, 591px 1452px $starcolor, 1773px 1411px $starcolor,
    1622px 1401px $starcolor, 534px 340px $starcolor, 1590px 284px $starcolor,
    1464px 528px $starcolor, 734px 1718px $starcolor, 1929px 1683px $starcolor,
    656px 480px $starcolor, 833px 705px $starcolor, 1567px 109px $starcolor,
    1055px 330px $starcolor, 1943px 1367px $starcolor, 1935px 1512px $starcolor,
    355px 1024px $starcolor, 1894px 218px $starcolor, 1703px 1772px $starcolor,
    781px 1394px $starcolor, 367px 42px $starcolor, 100px 690px $starcolor,
    1831px 458px $starcolor, 1884px 1878px $starcolor, 814px 1013px $starcolor;
  animation: animStar 120s linear infinite;
}
#stars2:after {
  z-index: -10;
  content: " ";
  position: absolute;
  top: 2000px;
  width: 2px;
  height: 2px;
  background: transparent;
  box-shadow: 1907px 1575px $starcolor, 893px 268px $starcolor,
    1819px 666px $starcolor, 366px 1985px $starcolor, 1736px 1062px $starcolor,
    1124px 45px $starcolor, 905px 1674px $starcolor, 1570px 711px $starcolor,
    255px 1747px $starcolor, 147px 1032px $starcolor, 865px 1813px $starcolor,
    1721px 1461px $starcolor, 202px 724px $starcolor, 1860px 812px $starcolor,
    634px 1410px $starcolor, 927px 1264px $starcolor, 1648px 620px $starcolor,
    1915px 1309px $starcolor, 731px 778px $starcolor, 91px 1185px $starcolor,
    829px 1003px $starcolor, 174px 1784px $starcolor, 1094px 1874px $starcolor,
    1464px 484px $starcolor, 1639px 1717px $starcolor, 959px 573px $starcolor,
    1686px 1287px $starcolor, 906px 356px $starcolor, 970px 499px $starcolor,
    626px 890px $starcolor, 1344px 1070px $starcolor, 1351px 544px $starcolor,
    708px 68px $starcolor, 1870px 130px $starcolor, 556px 1270px $starcolor,
    1432px 618px $starcolor, 769px 673px $starcolor, 1289px 1410px $starcolor,
    1499px 1969px $starcolor, 749px 1163px $starcolor, 1198px 198px $starcolor,
    399px 133px $starcolor, 1856px 1280px $starcolor, 904px 194px $starcolor,
    973px 1107px $starcolor, 1371px 1785px $starcolor, 989px 1835px $starcolor,
    1043px 1517px $starcolor, 787px 916px $starcolor, 1635px 1155px $starcolor,
    752px 524px $starcolor, 1926px 1279px $starcolor, 1052px 1163px $starcolor,
    719px 1963px $starcolor, 786px 519px $starcolor, 1440px 500px $starcolor,
    156px 1265px $starcolor, 1691px 429px $starcolor, 1349px 1474px $starcolor,
    736px 459px $starcolor, 248px 1678px $starcolor, 1136px 510px $starcolor,
    1317px 10px $starcolor, 1209px 1323px $starcolor, 54px 469px $starcolor,
    730px 1939px $starcolor, 960px 23px $starcolor, 112px 941px $starcolor,
    1852px 1522px $starcolor, 1993px 1972px $starcolor, 265px 129px $starcolor,
    222px 1897px $starcolor, 1766px 1804px $starcolor, 1530px 1786px $starcolor,
    1045px 432px $starcolor, 1916px 1980px $starcolor, 309px 1780px $starcolor,
    1420px 559px $starcolor, 1708px 103px $starcolor, 324px 1407px $starcolor,
    1175px 943px $starcolor, 80px 1221px $starcolor, 1016px 1933px $starcolor,
    318px 560px $starcolor, 190px 1489px $starcolor, 1095px 892px $starcolor,
    1975px 1191px $starcolor, 1197px 955px $starcolor, 1482px 873px $starcolor,
    1912px 300px $starcolor, 2000px 1636px $starcolor, 1473px 1808px $starcolor,
    507px 192px $starcolor, 924px 1300px $starcolor, 1485px 1636px $starcolor,
    41px 1822px $starcolor, 689px 120px $starcolor, 769px 273px $starcolor,
    1039px 976px $starcolor, 1057px 1520px $starcolor, 1417px 1187px $starcolor,
    512px 1507px $starcolor, 519px 45px $starcolor, 1207px 1687px $starcolor,
    1824px 1488px $starcolor, 1694px 31px $starcolor, 1859px 52px $starcolor,
    1368px 268px $starcolor, 190px 1404px $starcolor, 940px 1003px $starcolor,
    167px 942px $starcolor, 1641px 647px $starcolor, 1051px 654px $starcolor,
    233px 1640px $starcolor, 554px 511px $starcolor, 1705px 1866px $starcolor,
    240px 1430px $starcolor, 140px 668px $starcolor, 648px 1617px $starcolor,
    252px 101px $starcolor, 676px 1774px $starcolor, 889px 1698px $starcolor,
    595px 853px $starcolor, 249px 1768px $starcolor, 1091px 1529px $starcolor,
    223px 839px $starcolor, 239px 699px $starcolor, 1547px 356px $starcolor,
    249px 1130px $starcolor, 1209px 1946px $starcolor, 1967px 1274px $starcolor,
    430px 298px $starcolor, 1305px 134px $starcolor, 156px 91px $starcolor,
    1712px 264px $starcolor, 1256px 991px $starcolor, 1887px 1844px $starcolor,
    1957px 1275px $starcolor, 1718px 666px $starcolor, 1090px 543px $starcolor,
    933px 1411px $starcolor, 801px 323px $starcolor, 202px 1659px $starcolor,
    1117px 549px $starcolor, 290px 1859px $starcolor, 1380px 1516px $starcolor,
    557px 1165px $starcolor, 1953px 1758px $starcolor, 1901px 1407px $starcolor,
    1144px 347px $starcolor, 1640px 271px $starcolor, 1996px 43px $starcolor,
    838px 488px $starcolor, 1151px 1529px $starcolor, 306px 460px $starcolor,
    1666px 635px $starcolor, 1572px 633px $starcolor, 1797px 1076px $starcolor,
    1727px 1119px $starcolor, 474px 871px $starcolor, 1491px 1398px $starcolor,
    1301px 868px $starcolor, 1632px 454px $starcolor, 1611px 466px $starcolor,
    498px 1162px $starcolor, 796px 269px $starcolor, 1988px 747px $starcolor,
    502px 12px $starcolor, 276px 1260px $starcolor, 1536px 974px $starcolor,
    956px 656px $starcolor, 107px 701px $starcolor, 965px 491px $starcolor,
    1646px 247px $starcolor, 1515px 921px $starcolor, 1813px 519px $starcolor,
    697px 143px $starcolor, 591px 1452px $starcolor, 1773px 1411px $starcolor,
    1622px 1401px $starcolor, 534px 340px $starcolor, 1590px 284px $starcolor,
    1464px 528px $starcolor, 734px 1718px $starcolor, 1929px 1683px $starcolor,
    656px 480px $starcolor, 833px 705px $starcolor, 1567px 109px $starcolor,
    1055px 330px $starcolor, 1943px 1367px $starcolor, 1935px 1512px $starcolor,
    355px 1024px $starcolor, 1894px 218px $starcolor, 1703px 1772px $starcolor,
    781px 1394px $starcolor, 367px 42px $starcolor, 100px 690px $starcolor,
    1831px 458px $starcolor, 1884px 1878px $starcolor, 814px 1013px $starcolor;
}

@keyframes animStar {
  from {
    transform: translateY(-2000px);
  }
  to {
    transform: translateY(0px);
  }
}
</style>
