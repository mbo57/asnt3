FROM node:20.11.1-alpine
ARG frontend_src_path_container

ENV FRONTEND_SRC_PATH_CONTAINER $frontend_src_path_container

WORKDIR ${FRONTEND_SRC_PATH_CONTAINER}
CMD ["sh", "-c", "yarn && yarn dev"]
