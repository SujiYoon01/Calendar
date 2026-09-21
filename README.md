      subgroup:"핵심인력 확보", weight:"", target:"위성영상 AI 솔루션\n수출 기반 구축", sgMergeUp:false, targetMergeUp:true, weightMergeUp:true,

    var sgSpans = computeSpans(list, "sgMergeUp");
    var targetSpans = computeSpans(list, "targetMergeUp");
    var weightSpans = (function(){
      var arr = new Array(list.length), i = 0;
      function wmu(r){ return r.weightMergeUp !== undefined ? r.weightMergeUp : r.sgMergeUp; }
      while (i < list.length){
        var span = 1;
        while (i + span < list.length && wmu(list[i + span])) span++;
        arr[i] = span;
        for (var k = 1; k < span; k++) arr[i + k] = 0;
        i += span;
      }
      return arr;
    })();


      if (sgSpans[pos] > 0){
        if (!groupAbsorbsSub[pos]){
          var hasGrades = !row.isSummary && row.gradeSections;
          rowsHTML += '<td class="c-subgroup' + (hasGrades ? ' has-grades' : '') + '" rowspan="' + sgSpans[pos] + '"' + (hasGrades ? ' data-act="showgrades" data-idx="' + idx + '" title="클릭하면 등급별 목표를 볼 수 있어요"' : '') + '>' + (row.subgroup !== "" ? nl2br(row.subgroup) : '') + '</td>';
        }
      }
      if (weightSpans[pos] > 0){
        rowsHTML += '<td class="c-weight" rowspan="' + weightSpans[pos] + '">' + esc(row.weight) + '</td>';
      }
