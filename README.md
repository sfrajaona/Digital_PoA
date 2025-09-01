

Issues
=================

- Problem1: there are always forced actions (revocation request) by D 
    - Solution11: added enacting possibilities for D, so that D can do some actions
rather than revoking after delegating.   But this did not work:
after request_deleg, request_action, and while these 2 are still under processing
D cannot do anything but request_revoke hence enacting for A cannot be enabled
    - Solution12: add idle action, but they can only fire after some requests has been made
when a request has been fulfilled, idling cannot be enabled,
hence the model size does not blow up
    - Solution13: add idle action, but limit the number of idling times

- Problem2: once one revoked, there could be another delegation
hence the formula AG (revoked -> AG!executed) fails
    - Solution21: once revoked, cannot redo delegation

- Problem with nonsync actions:
when actions are non-synched, 
and L do register_revoke_A_att_of_D
and simultaneously an action is requested

- Problem with Safety under Revocation : when the guard (!revoked_A_by_D) 
- is omitted from the execute action (in module V_enact) 
then there is a possibility that an action 
that was granted  before the revocation was requested
would still execute after the revocation occurred 
i.e., the "Safety under revocation" formula "AG (revoked_A_by_D -> AG ¬executed_A)" fails

- Problem3: the original end-to-end correctness with strategic operator is false
in our model when the strategic operator is <<A,V>>, although it is true
when we use all players <<D,A,L,V>> 
    - SOLVED: corrected the model, and put the exact same guards as in the
        model
