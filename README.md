# Rova is a high quality onchain launchpad focused on small ticket, global retail public token sales. #

rova-contracts

- Handling refunds - Users can intentionally claim refunds on their own for launch groups that have been completed. We also allow anyone with the operator role to trigger batch refunds for unfinalized participations. This is so we can make sure to process all refunds on behalf of users, but allow users the option to get their refund earlier than our automated refund system.
- Batch actions - Finalizing winning participations and handling refunds for a set of participations can be done in batch to reduce the number of automated transactions our backend system needs to process. It can be assumed that the batch count submitted will not go over the block gas limit.
- Launch group setting updates are intended to be handled manually to coordinate with relevant teams involved in the launch and backend processes.

rova-movement-contracts

- These were designed to be a much simpler, scaled-down version of rova-contracts for the following reasons:
    - We do not plan to handle alternative coin payment methods other than native MOVE on Movement.
    - Only FCFS launch structure is supported. Once a user funds the sale contract, their participation in the sale is considered finalized. We do not need to support sale commitment updates, cancellations, or refunds.
    - We do not plan to support multiple launch groups. All users participating will fall under one bucket with the same start/end time and token price.
___



