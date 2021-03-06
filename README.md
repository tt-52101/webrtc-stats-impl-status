# webrtc-stats-impl-status

> https://w3c.github.io/webrtc-stats/

This repository lists current WebRTC Statistics implementaion status for latest browser versions.

## Settings

- pc1: send+recv 1 video, 1 audio, and 1 datachannel w/  TURN
- pc2: send+recv 1 video, 1 audio, and 1 datachannel w/o TURN

See [./docs/main.js](./docs/main.js) for details.

## Notes

- ✅ means that `key` exists in the report
- There are much more stats-types in the spec
- Some of stats report has kind-specific props even in the same stats-type
  - e.g. `inbound-rtp` with `kind = audio` and `kind = video` have different props
- Type `track` is obsolete stats
  - will be replaced with `sender`, `receiver` stats in the future
- Some of props are also obsolete
  - e.g. `networkType` in `local-candidate` report

---

## RTCStatsType

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| transport | ✅ | ✅ |  | ✅ |
| stream | ✅ | ✅ |  |  |
| track | ✅ | ✅ |  | ✅ |
| codec | ✅ | ✅ |  | ✅ |
| certificate | ✅ | ✅ |  | ✅ |
| media-source | ✅ | ✅ |  |  |
| data-channel | ✅ | ✅ |  | ✅ |
| candidate-pair | ✅ | ✅ | ✅ | ✅ |
| local-candidate | ✅ | ✅ | ✅ |  |
| remote-candidate | ✅ | ✅ | ✅ | ✅ |
| inbound-rtp | ✅ | ✅ | ✅ | ✅ |
| outbound-rtp | ✅ | ✅ | ✅ | ✅ |
| peer-connection | ✅ | ✅ |  | ✅ |
| remote-inbound-rtp | ✅ | ✅ | ✅ |  |
| remote-outbound-rtp |  |  | ✅ |  |

## Details

### transport

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| type | ✅ | ✅ |  | ✅ |
| dtlsState | ✅ | ✅ |  |  |
| bytesSent | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| srtpCipher | ✅ | ✅ |  |  |
| dtlsCipher | ✅ | ✅ |  |  |
| tlsVersion | ✅ | ✅ |  |  |
| bytesReceived | ✅ | ✅ |  | ✅ |
| localCertificateId | ✅ | ✅ |  | ✅ |
| remoteCertificateId | ✅ | ✅ |  | ✅ |
| selectedCandidatePairId | ✅ | ✅ |  | ✅ |
| selectedCandidatePairChanges | ✅ | ✅ |  |  |

### stream

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  |  |
| type | ✅ | ✅ |  |  |
| trackIds | ✅ | ✅ |  |  |
| timestamp | ✅ | ✅ |  |  |
| streamIdentifier | ✅ | ✅ |  |  |

### track

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| kind | ✅ | ✅ |  |  |
| type | ✅ | ✅ |  | ✅ |
| ended | ✅ | ✅ |  | ✅ |
| detached | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| framesSent | ✅ | ✅ |  | ✅ |
| frameWidth | ✅ | ✅ |  | ✅ |
| audioLevel | ✅ | ✅ |  | ✅ |
| frameHeight | ✅ | ✅ |  | ✅ |
| remoteSource | ✅ | ✅ |  | ✅ |
| mediaSourceId | ✅ | ✅ |  |  |
| framesDropped | ✅ | ✅ |  | ✅ |
| framesDecoded | ✅ | ✅ |  | ✅ |
| echoReturnLoss |  |  |  | ✅ |
| hugeFramesSent | ✅ | ✅ |  |  |
| framesReceived | ✅ | ✅ |  | ✅ |
| trackIdentifier | ✅ | ✅ |  | ✅ |
| concealedSamples | ✅ | ✅ |  |  |
| totalAudioEnergy | ✅ | ✅ |  |  |
| concealmentEvents | ✅ | ✅ |  |  |
| jitterBufferDelay | ✅ | ✅ |  |  |
| totalSamplesDuration | ✅ | ✅ |  |  |
| totalSamplesReceived | ✅ | ✅ |  |  |
| silentConcealedSamples | ✅ | ✅ |  |  |
| jitterBufferEmittedCount | ✅ | ✅ |  |  |
| echoReturnLossEnhancement |  |  |  | ✅ |
| removedSamplesForAcceleration | ✅ | ✅ |  |  |
| insertedSamplesForDeceleration | ✅ | ✅ |  |  |

### codec

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| type | ✅ | ✅ |  | ✅ |
| mimeType | ✅ | ✅ |  | ✅ |
| clockRate | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| payloadType | ✅ | ✅ |  | ✅ |

### certificate

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| type | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| fingerprint | ✅ | ✅ |  | ✅ |
| base64Certificate | ✅ | ✅ |  | ✅ |
| fingerprintAlgorithm | ✅ | ✅ |  | ✅ |

### media-source

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  |  |
| kind | ✅ | ✅ |  |  |
| type | ✅ | ✅ |  |  |
| width | ✅ | ✅ |  |  |
| height | ✅ | ✅ |  |  |
| timestamp | ✅ | ✅ |  |  |
| audioLevel | ✅ | ✅ |  |  |
| framesPerSecond | ✅ | ✅ |  |  |
| trackIdentifier | ✅ | ✅ |  |  |
| totalAudioEnergy | ✅ | ✅ |  |  |
| totalSamplesDuration | ✅ | ✅ |  |  |

### data-channel

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| type | ✅ | ✅ |  | ✅ |
| state | ✅ | ✅ |  | ✅ |
| label | ✅ | ✅ |  | ✅ |
| protocol | ✅ | ✅ |  | ✅ |
| bytesSent | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| messagesSent | ✅ | ✅ |  | ✅ |
| bytesReceived | ✅ | ✅ |  | ✅ |
| datachannelid | ✅ | ✅ |  | ✅ |
| messagesReceived | ✅ | ✅ |  | ✅ |

### candidate-pair

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ | ✅ | ✅ |
| type | ✅ | ✅ | ✅ | ✅ |
| state | ✅ | ✅ | ✅ | ✅ |
| selected |  |  | ✅ |  |
| readable |  |  | ✅ |  |
| writable | ✅ | ✅ | ✅ | ✅ |
| priority | ✅ | ✅ | ✅ | ✅ |
| bytesSent | ✅ | ✅ | ✅ | ✅ |
| nominated | ✅ | ✅ | ✅ | ✅ |
| timestamp | ✅ | ✅ | ✅ | ✅ |
| transportId | ✅ | ✅ | ✅ | ✅ |
| requestsSent | ✅ | ✅ |  | ✅ |
| responsesSent | ✅ | ✅ |  | ✅ |
| bytesReceived | ✅ | ✅ | ✅ | ✅ |
| requestsReceived | ✅ | ✅ |  | ✅ |
| localCandidateId | ✅ | ✅ | ✅ | ✅ |
| responsesReceived | ✅ | ✅ |  | ✅ |
| remoteCandidateId | ✅ | ✅ | ✅ | ✅ |
| totalRoundTripTime | ✅ | ✅ |  | ✅ |
| consentRequestsSent | ✅ | ✅ |  |  |
| currentRoundTripTime | ✅ | ✅ |  | ✅ |
| lastPacketSentTimestamp |  |  | ✅ |  |
| availableOutgoingBitrate | ✅ | ✅ |  | ✅ |
| lastPacketReceivedTimestamp |  |  | ✅ |  |

### local-candidate

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| ip | ✅ | ✅ |  |  |
| id | ✅ | ✅ | ✅ |  |
| port | ✅ | ✅ | ✅ |  |
| type | ✅ | ✅ | ✅ |  |
| address |  |  | ✅ |  |
| deleted | ✅ | ✅ |  |  |
| priority | ✅ | ✅ | ✅ |  |
| protocol | ✅ | ✅ | ✅ |  |
| isRemote | ✅ | ✅ |  |  |
| timestamp | ✅ | ✅ | ✅ |  |
| networkType | ✅ | ✅ |  |  |
| transportId | ✅ | ✅ |  |  |
| candidateType | ✅ | ✅ | ✅ |  |
| relayProtocol | ✅ | ✅ | ✅ |  |

### remote-candidate

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| ip | ✅ | ✅ |  |  |
| id | ✅ | ✅ | ✅ | ✅ |
| port | ✅ | ✅ | ✅ | ✅ |
| type | ✅ | ✅ | ✅ | ✅ |
| address |  |  | ✅ | ✅ |
| deleted | ✅ | ✅ |  | ✅ |
| priority | ✅ | ✅ | ✅ | ✅ |
| protocol | ✅ | ✅ | ✅ | ✅ |
| isRemote | ✅ | ✅ |  |  |
| timestamp | ✅ | ✅ | ✅ | ✅ |
| transportId | ✅ | ✅ |  | ✅ |
| candidateType | ✅ | ✅ | ✅ | ✅ |

### inbound-rtp

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ | ✅ | ✅ |
| kind | ✅ | ✅ | ✅ |  |
| ssrc | ✅ | ✅ | ✅ | ✅ |
| type | ✅ | ✅ | ✅ | ✅ |
| qpSum | ✅ | ✅ |  | ✅ |
| jitter | ✅ | ✅ | ✅ | ✅ |
| codecId | ✅ | ✅ |  | ✅ |
| trackId | ✅ | ✅ |  | ✅ |
| remoteId |  |  | ✅ |  |
| pliCount | ✅ | ✅ | ✅ | ✅ |
| firCount | ✅ | ✅ | ✅ | ✅ |
| isRemote | ✅ | ✅ |  | ✅ |
| nackCount | ✅ | ✅ | ✅ | ✅ |
| mediaType | ✅ | ✅ | ✅ | ✅ |
| timestamp | ✅ | ✅ | ✅ | ✅ |
| bitrateMean |  |  | ✅ |  |
| packetsLost | ✅ | ✅ | ✅ | ✅ |
| transportId | ✅ | ✅ |  | ✅ |
| framerateMean |  |  | ✅ |  |
| bitrateStdDev |  |  | ✅ |  |
| framesDecoded | ✅ | ✅ | ✅ | ✅ |
| bytesReceived | ✅ | ✅ | ✅ | ✅ |
| framerateStdDev |  |  | ✅ |  |
| totalDecodeTime | ✅ | ✅ |  |  |
| packetsReceived | ✅ | ✅ | ✅ | ✅ |
| discardedPackets |  |  | ✅ |  |
| keyFramesDecoded | ✅ | ✅ |  |  |
| fecPacketsReceived | ✅ | ✅ |  |  |
| headerBytesReceived | ✅ | ✅ |  |  |
| fecPacketsDiscarded | ✅ | ✅ |  |  |
| totalInterFrameDelay | ✅ | ✅ |  |  |
| decoderImplementation | ✅ | ✅ |  |  |
| estimatedPlayoutTimestamp | ✅ | ✅ |  |  |
| totalSquaredInterFrameDelay | ✅ | ✅ |  |  |
| lastPacketReceivedTimestamp | ✅ | ✅ |  |  |

### outbound-rtp

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ | ✅ | ✅ |
| kind | ✅ | ✅ | ✅ |  |
| ssrc | ✅ | ✅ | ✅ | ✅ |
| type | ✅ | ✅ | ✅ | ✅ |
| qpSum | ✅ | ✅ | ✅ | ✅ |
| codecId | ✅ | ✅ |  | ✅ |
| trackId | ✅ | ✅ |  | ✅ |
| pliCount | ✅ | ✅ | ✅ | ✅ |
| firCount | ✅ | ✅ | ✅ | ✅ |
| remoteId | ✅ | ✅ | ✅ |  |
| isRemote | ✅ | ✅ |  | ✅ |
| nackCount | ✅ | ✅ | ✅ | ✅ |
| bytesSent | ✅ | ✅ | ✅ | ✅ |
| mediaType | ✅ | ✅ | ✅ | ✅ |
| timestamp | ✅ | ✅ | ✅ | ✅ |
| bitrateMean |  |  | ✅ |  |
| contentType | ✅ | ✅ |  |  |
| packetsSent | ✅ | ✅ | ✅ | ✅ |
| transportId | ✅ | ✅ |  | ✅ |
| framerateMean |  |  | ✅ |  |
| droppedFrames |  |  | ✅ |  |
| bitrateStdDev |  |  | ✅ |  |
| framesEncoded | ✅ | ✅ | ✅ | ✅ |
| mediaSourceId | ✅ | ✅ |  |  |
| framerateStdDev |  |  | ✅ |  |
| totalEncodeTime | ✅ | ✅ |  |  |
| headerBytesSent | ✅ | ✅ |  |  |
| keyFramesEncoded | ✅ | ✅ |  |  |
| totalPacketSendDelay | ✅ | ✅ |  |  |
| encoderImplementation | ✅ | ✅ |  |  |
| retransmittedBytesSent | ✅ | ✅ |  |  |
| qualityLimitationReason | ✅ | ✅ |  |  |
| totalEncodedBytesTarget | ✅ | ✅ |  |  |
| retransmittedPacketsSent | ✅ | ✅ |  |  |
| qualityLimitationResolutionChanges | ✅ | ✅ |  |  |

### peer-connection

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ |  | ✅ |
| type | ✅ | ✅ |  | ✅ |
| timestamp | ✅ | ✅ |  | ✅ |
| dataChannelsClosed | ✅ | ✅ |  | ✅ |
| dataChannelsOpened | ✅ | ✅ |  | ✅ |

### remote-inbound-rtp

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id | ✅ | ✅ | ✅ |  |
| kind | ✅ | ✅ | ✅ |  |
| ssrc | ✅ | ✅ | ✅ |  |
| type | ✅ | ✅ | ✅ |  |
| jitter | ✅ | ✅ | ✅ |  |
| localId | ✅ | ✅ | ✅ |  |
| codecId | ✅ | ✅ |  |  |
| mediaType |  |  | ✅ |  |
| timestamp | ✅ | ✅ | ✅ |  |
| packetsLost | ✅ | ✅ | ✅ |  |
| transportId | ✅ | ✅ |  |  |
| bytesReceived |  |  | ✅ |  |
| roundTripTime | ✅ | ✅ | ✅ |  |
| packetsReceived |  |  | ✅ |  |

### remote-outbound-rtp

|  | chrome v81 | edge v81 | firefox v76 | safari v13.1 |
| --: | :--: | :--: | :--: | :--: |
| id |  |  | ✅ |  |
| ssrc |  |  | ✅ |  |
| kind |  |  | ✅ |  |
| type |  |  | ✅ |  |
| localId |  |  | ✅ |  |
| bytesSent |  |  | ✅ |  |
| mediaType |  |  | ✅ |  |
| timestamp |  |  | ✅ |  |
| packetsSent |  |  | ✅ |  |
