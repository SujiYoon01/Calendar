  // 이번 달을 5주로 나눠서 CUR_WEEK 주차만 칠함 (1~5)
  var CUR_WEEK = 2;
  function weekBand(s, span){
    var w = 1 / span, off = (CUR_M - s) / span;
    var a = (off + (CUR_WEEK - 1) / 5 * w) * 100, b = (off + CUR_WEEK / 5 * w) * 100;
    return '--wk-a:' + a.toFixed(2) + '%;--wk-b:' + b.toFixed(2) + '%';
  }
  function weekStripHTML(){
    var h = '<div class="wk-strip">';
    for (var k = 1; k <= 5; k++) h += '<i' + (k === CUR_WEEK ? ' class="on"' : '') + '></i>';
    return h + '</div>';
  }


