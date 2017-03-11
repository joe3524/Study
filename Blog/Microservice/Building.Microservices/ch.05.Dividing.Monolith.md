Monolith에서 MSA로 나누는 단계를 먼저 Database Schema 부터 나눈 뒤 서비스를 나누라고 가이드되어 있다.
이점에서는 동의를 하기 힘들다. DB를 나눈다는건 그 기간동안 서비스를 중단해야 할만큼 큰 작업이기 때문이다.
그리고 DB를 나누면 JOIN 작업에 대해서 엄청 불편해질텐데, 그것을 모두 감수하라고 하는 말에 동의가 되지 않는다.
책에서는 다른 서비스의 데이터에 접근하는건 API를 통해서 가져오고 JOIN은 프로그램 상으로 구현하라고 되어 있다.

트랜잭션 성격의 작업또한 직접 구현을 해야한다면서 여러 가지 방법을 제시하지만 구체적인건 하나도 없다.
결국 하는 말이 여기에 대한 은총알은 없다면서 어떠한 방법도 완벽하지 않고 오류가 발생할 수 있다는 것이다.
이 말에는 전적으로 동의를 하지만, 트랜잭션을 DB 단에서 해결하는 것이 가장 완벽한데, 그걸 포기하고 직접 구현하면서까지 그것도 완벽하지 못하다는 것을 알고도 그렇게 나누는게 과연 옳은지에 대해서는 솔직히 동의할 수 없다.

모노리스로 시스템이 점점 커지는게 죄약이 아니라고 말한다.
단지 어느 시점에 분리 작업이 필요한지에 대해서 인식하는 것이 그 핵심이다. 이 말에 위안을 받는 사람들이 많을 것 같다. 처음부터 MSA로 시스템을 설계하여 접근하는게 쉽지는 않을 것이다.



